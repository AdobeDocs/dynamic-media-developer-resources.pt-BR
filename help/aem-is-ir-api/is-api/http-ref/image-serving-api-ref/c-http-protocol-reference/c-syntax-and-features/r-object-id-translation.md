---
description: O Servidor de imagens fornece um mecanismo para converter IDs de objeto externo em IDs de objeto (catálogo) específicas da localidade. O aplicativo principal é o de fornecer conteúdo específico de local e conteúdo compartilhado entre várias localidades, sem que o aplicativo cliente precise saber as IDs de objeto específicas da localidade.
solution: Experience Manager
title: Conversão da ID do objeto
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7a3bd6a1-2ad4-4da2-944c-489b7d18fdc1
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 0%

---

# Conversão da ID do objeto{#object-id-translation}

O Servidor de imagens fornece um mecanismo para converter IDs de objeto externo em IDs de objeto (catálogo) específicas da localidade. O aplicativo principal é o de fornecer conteúdo específico de local e conteúdo compartilhado entre várias localidades, sem que o aplicativo cliente precise saber as IDs de objeto específicas da localidade.

O aplicativo pode ser gravado usando apenas IDs de objeto global, e o Servidor de imagens substitui automaticamente imagens específicas da localidade e outros conteúdos disponíveis.

A variável *`locale`* é especificado em solicitações do Servidor de imagens com o `locale=` comando.

>[!NOTE]
>
>A tradução da ID do objeto é aplicável somente para uso do Servidor de imagens com base no catálogo. Não é possível traduzir nomes de arquivo.

## Escopo {#section-66fcd5bd467c4eeaa1574583cbe9756d}

Todas as referências a entradas em catálogos de imagem, SVG e conteúdo estático são consideradas para fontes de tradução e as referências de perfil ICC não são traduzidas. Além do *`object`* no caminho de [!DNL /is/image] e [!DNL /is/static requests], esses comandos e atributos de catálogo estão sujeitos à tradução de ID: `src=`, `mask=`, `template=`, `defaultImage=`, `attribute::DefaultImage`, e `attribute::Watermark`.

## O mapa de tradução de ID {#section-9e417b352c314dfe94e831fdd62cddc8}

`attribute::LocaleMap` define as regras usadas pelo servidor para determinar a ID do conteúdo localizado, fornecidas como entradas para a ID do objeto genérico e a `locale=` valor.

`attribute::LocaleMap` consiste em uma lista de entradas *localidades* (correspondendo aos valores especificados com `locale=`), cada um com nenhum ou mais sufixos de localidade de saída ( `*`locSuffixes`*`).

Por exemplo, `attribute::LocaleMap` pode ser semelhante a:

`en,_E,|en_us,_E,|en_uk,_E,|fr,_F,|de,_D,|de_at,_D,|de_de,_D,|,_E,`

A solicitação `/is/image/myCat/myImg?locale=de_de` retornaria a imagem associada à entrada do catálogo `myCat/myImg_D` (supondo que essa entrada de catálogo exista).

Consulte a descrição de `attribute::LocaleMap` para obter detalhes.

## O processo de tradução {#section-1f64db17e9f644d88e09853670e14a16}

Dado o exemplo acima, o servidor primeiro procura pela variável *`locale`* &quot; `de_de`&quot; no mapa de tradução de ID. Em seguida, repete *`locSuffixes`* associado a esta entrada neste caso &quot; `_D`&quot; e &quot;&quot; (sufixo vazio). Para cada iteração, o sufixo é anexado à ID da imagem e a ID resultante é testada para existência no catálogo. Se encontrada, essa entrada de catálogo será usada, caso contrário, a próxima será testada. Neste exemplo, essas entradas são verificadas: `myCat/myImg_D`, e `myCat/myImg`. Se nenhuma correspondência for encontrada, o servidor retornará um erro ou uma imagem padrão (se configurada).

## Localidades desconhecidas {#section-b2f3c83f2dc845d69b5908107b775537}

No exemplo acima, `attribute::LocaleMap` inclui um vazio *`locale`* que define a regra de conversão padrão, usada para `locale=` valores (ou seja, aqueles não listados explicitamente no mapa de tradução). Se este mapa de tradução foi aplicado à solicitação `/is/image/myCat/myImg?locale=ja`, resolveria para `myCat/myImg_E`, se existir, ou de outra forma `myCat/myImg`.

Se um mapa de tradução não especificar uma regra de tradução padrão, um erro será retornado para todas as solicitações com nomes desconhecidos `locale=` valores.

## Exemplos {#section-cc40bb00ee9248bb8cb23e17d7a5984c}

**Pesquisa em várias camadas**

Geralmente, é desejável agrupar locais (por exemplo, Europeu, Oriente Médio, América do Norte) para abordar padrões regionais. Isso pode ser feito com uma pesquisa em várias camadas.

Neste exemplo, queremos oferecer suporte a coleções para uso no Oeste e no Oriente Médio. Ambas as coleções se baseiam na coleção de imagens genérica e adicionam ou modificam algumas imagens. Ambas as coleções são então refinadas para localidades específicas ( `m1`, `m2` para duas variantes do médio oriente, e `w1`, `w2`, e `w3` para três localidades ocidentais), exceto que as imagens são compartilhadas para `w1` e `w3`. Locais desconhecidos são mapeados somente para a coleção genérica e não têm acesso a imagens específicas do local.

`attribute::LocaleMap: w1,-W,|w2,-W2,-W,|w3,-W,|m1,-M1,-M,|m2,-M2,-M,|,`

A tabela a seguir ilustra quais entradas de catálogo são consideradas e a ordem em que são consideradas para a ID de entrada genérica `myImg`:

<table id="table_97EB13E3DB9B48D3A4184D5ECC8E9F86"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>localidade</i> </b> </th> 
   <th class="entry"> <b>IDs de catálogo a serem pesquisadas</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> w1, w3 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> w2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-W2, myImg-W, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m1 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M1, myImg-M, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> m2 </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg-M2, myImg-M, myImg </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>todos os outros </p> </td> 
   <td> <p> <span class="codeph"> myImg </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Pesquisar IDs específicas**

Algumas convenções de nomenclatura de imagem podem não suportar IDs de imagem genéricas internamente. As IDs genéricas da solicitação sempre devem ser mapeadas para uma ID específica no catálogo; geralmente, a ID específica exata pode não ser conhecida.

Neste exemplo, imagens para todos os idiomas podem ter `_1`, `_2`ou `_3` sufixo. Imagens específicas para localidades francesas podem ter `_22` ou `_23` sufixo e imagens específicas para locais alemães podem ter `_470` ou `_480` sufixo.

`attribute::LocaleMap: ,_1,_2,_3|fr,_22,_23,_1,_2,_3|de,_470,_480,_1,_2,_3| de_at,_470,_480,_1,_2,_3| de_de,_470,_480,_1,_2,_3`

A tabela a seguir ilustra quais entradas de catálogo são consideradas e a ordem em que são consideradas para a ID de entrada genérica `myImg`:

<table id="table_A7EE4AA0F1C24284B83CC4B40622D24F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>localidade</i> </b> </th> 
   <th class="entry"> <b>IDs de saída a serem pesquisadas</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fr </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_22, myImg_23, myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> de </span>, <span class="codeph"> de_at </span>, <span class="codeph"> de_de </span> </p> </td> 
   <td> <p> <span class="codeph"> myImg_470, myImg_480, myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>todos os outros </p> </td> 
   <td> <p> <span class="codeph"> myImg_1, myImg_2, myImg_3 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Consulte também {#section-05893816c66a406d89f9bfd6ace8d47a}

[attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318) , [attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b), [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [req=xlate](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
