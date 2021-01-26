---
description: O Serviço de imagem fornece um mecanismo para traduzir IDs de objetos externos para IDs de objetos (catálogo) específicos da localidade. O aplicativo principal é fornecer conteúdo e conteúdo específicos à localidade compartilhados entre várias localidades, sem que o aplicativo cliente precise conhecer as IDs de objeto específicas à localidade.
seo-description: O Serviço de imagem fornece um mecanismo para traduzir IDs de objetos externos para IDs de objetos (catálogo) específicos da localidade. O aplicativo principal é fornecer conteúdo e conteúdo específicos à localidade compartilhados entre várias localidades, sem que o aplicativo cliente precise conhecer as IDs de objeto específicas à localidade.
seo-title: Tradução da ID do objeto
solution: Experience Manager
title: Tradução da ID do objeto
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 8b4c2f44-033a-428a-b505-af389865c70a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '741'
ht-degree: 0%

---


# Tradução da ID do objeto{#object-id-translation}

O Serviço de imagem fornece um mecanismo para traduzir IDs de objetos externos para IDs de objetos (catálogo) específicos da localidade. O aplicativo principal é fornecer conteúdo e conteúdo específicos à localidade compartilhados entre várias localidades, sem que o aplicativo cliente precise conhecer as IDs de objeto específicas à localidade.

O aplicativo pode ser gravado usando apenas IDs de objeto globais e o Serviço de imagem substituirá automaticamente imagens específicas da localidade e outro conteúdo, quando disponível.

O *`locale`* é especificado nas solicitações do Servidor de imagens com o comando `locale=`.

>[!NOTE]
>
>A tradução da ID do objeto só é aplicável para o uso baseado em catálogo do Serviço de imagem. Nomes de arquivo não podem ser convertidos.

## Âmbito {#section-66fcd5bd467c4eeaa1574583cbe9756d}

Todas as referências a entradas em catálogos de imagem, SVG e conteúdo estático são consideradas para fontes de tradução e referências de perfil ICC não são traduzidas. Além de *`object`* no caminho de [!DNL /is/image] e [!DNL /is/static requests], esses comandos e atributos de catálogo estão sujeitos à tradução da ID: `src=`, `mask=`, `template=`, `defaultImage=`, `attribute::DefaultImage` e `attribute::Watermark`.

## O mapa de tradução de ID {#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap` define as regras usadas pelo servidor para determinar a ID do conteúdo localizado, considerando como entradas a ID do objeto genérico e o  `locale=` valor.

`attribute::LocaleMap` consiste em uma lista de  *localidades*  de entrada (correspondendo aos valores especificados com  `locale=`), cada uma com nenhum ou mais sufixos de localidade de saída (  `*`locSuffixes`*`).

Por exemplo, `attribute::LocaleMap` pode ser semelhante a:

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

A solicitação `/is/image/myCat/myImg?locale=de_de` retornaria a imagem associada à entrada do catálogo `myCat/myImg_D` (supondo que tal entrada de catálogo exista).

Consulte a descrição de `attribute::LocaleMap` para obter detalhes.

## O processo de tradução {#section-1f64db17e9f644d88e09853670e14a16}

Dado o exemplo acima, o servidor procura primeiro *`locale`* &quot; `de_de`&quot; no mapa de tradução de ID. Em seguida, ele repete o *`locSuffixes`* associado a essa entrada - neste caso, &quot; `_D`&quot; e &quot;&quot; (sufixo vazio). Para cada repetição, o sufixo é anexado à ID da imagem e a ID resultante testada para a existência no catálogo. Se encontrada, essa entrada de catálogo será usada, caso contrário, a próxima será testada. Neste exemplo, essas entradas são verificadas: `myCat/myImg_D` e `myCat/myImg`. Se nenhuma correspondência for encontrada, o servidor retornará um erro ou uma imagem padrão (se configurado).

## Códigos de idioma desconhecidos {#section-b2f3c83f2dc845d69b5908107b775537}

No exemplo acima, `attribute::LocaleMap` inclui um *`locale`* vazio que define a regra de conversão padrão, usada para valores `locale=` desconhecidos (ou seja, aqueles não listados explicitamente no mapa de conversão). Se esse mapa de tradução fosse aplicado à solicitação `/is/image/myCat/myImg?locale=ja`, resolveria para `myCat/myImg_E`, se existir, ou `myCat/myImg`.

Se um mapa de tradução não especificar uma regra de conversão padrão, um erro será retornado para todas as solicitações com valores `locale=` desconhecidos.

## Exemplos {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**Pesquisa em várias camadas**

Muitas vezes é desejável agrupar localidades (por exemplo, europeias, do Oriente Médio e norte-americanas) para atender aos padrões regionais. Isso pode ser feito com uma pesquisa em várias camadas.

Neste exemplo, queremos oferecer suporte a coleções para uso no Oriente Médio e Ocidental. Ambas as coleções são baseadas na coleção de imagens genérica e ambas adicionam ou modificam algumas imagens. Ambas as coleções são posteriormente refinadas para localidades específicas ( `m1`, `m2` para duas variantes do Oriente Médio e `w1`, `w2` e `w3` para três localidades Ocidentais), exceto que as imagens são compartilhadas para `w1` e `w3`. As localidades desconhecidas são mapeadas apenas para a coleção genérica e não têm acesso a imagens específicas da localidade.

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

A tabela a seguir ilustra quais entradas de catálogo serão consideradas e a ordem em que serão consideradas para a ID de entrada genérica `myImg`:

<table id="table_97EB13E3DB9B48D3A4184D5ECC8E9F86"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b>IDs de catálogo a serem pesquisadas</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> w1, w3  </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W, myImg  </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> w2  </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W2, myImg-W, myImg  </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m1  </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M1, myImg-M, myImg  </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m2  </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M2, myImg-M, myImg  </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>todos os outros </p> </td> 
   <td> <p> <span class="codeph"> myImg  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Procurar IDs específicas**

Algumas convenções de nomenclatura de imagem podem não suportar IDs de imagem genéricas internamente. As IDs genéricas da solicitação devem sempre ser mapeadas para uma ID específica no catálogo; geralmente, a ID específica exata pode não ser conhecida.

Neste exemplo, as imagens para todos os idiomas podem ter o sufixo `_1`, `_2` ou `_3`. As imagens específicas para localidades francesas podem ter o sufixo `_22` ou `_23`, e as imagens específicas para localidades alemãs podem ter o sufixo `_470` ou `_480`.

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

A tabela a seguir ilustra quais entradas de catálogo são consideradas e a ordem em que são consideradas para a ID de entrada genérica `myImg`:

<table id="table_A7EE4AA0F1C24284B83CC4B40622D24F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>locale</i> </b> </th> 
   <th class="entry"> <b>IDs de saída a serem pesquisadas</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fr  </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_22, myImg_23, myImg_1, myImg_2, myImg_3  </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> de  </span>,  <span class="codeph"> de_at  </span>,  <span class="codeph"> de_de  </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470, myImg_480, myImg_1, myImg_2, myImg_3  </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>todos os outros </p> </td> 
   <td> <p> <span class="codeph"> myImg_1, myImg_2, myImg_3  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Consulte também {#section-05893816c66a406d89f9bfd6ace8d47a}

[atributo::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318) ,  [atributo::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b),  [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb),  [req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
