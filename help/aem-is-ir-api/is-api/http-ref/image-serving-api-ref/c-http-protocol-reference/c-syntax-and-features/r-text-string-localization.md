---
description: A localização da string de texto permite que catálogos de imagem contenham várias representações específicas da localidade para o mesmo valor da string.
seo-description: A localização da string de texto permite que catálogos de imagem contenham várias representações específicas da localidade para o mesmo valor da string.
seo-title: Localização da string de texto
solution: Experience Manager
title: Localização da string de texto
topic: Scene7 Image Serving - Image Rendering API
uuid: bdff2403-e3bb-4b3f-a8d7-bb108c1fbee8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 0%

---


# Localização da string de texto{#text-string-localization}

A localização da string de texto permite que catálogos de imagem contenham várias representações específicas da localidade para o mesmo valor da string.

O servidor retorna ao cliente a representação que corresponde à localidade especificada com `locale=`, evitando assim a localização do lado do cliente e permitindo que os aplicativos alternem localidades simplesmente enviando o valor `locale=` apropriado com as solicitações de texto IS.

## Âmbito {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

A localização de string de texto é aplicada a todos os elementos de string que incluem o token de localização ` ^loc= *`locId`*^` nos seguintes campos de catálogo:

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Campo Catálogo</b> </th> 
   <th class="entry"> <b>Elemento de string no campo</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::ImageSet  </span> </p> </td> 
   <td> <p>Qualquer subelemento que contenha uma string traduzível (delimitada por qualquer combinação de separadores ',' ';' ':' e/ou o start/fim do campo). </p> <p> Um valor de cor <span class="codeph"> 0xrrggbb </span> no início de um campo localizável é excluído da localização e passado sem modificação. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::Mapa  </span> </p> </td> 
   <td> <p>Qualquer valor de atributo entre aspas simples ou duplos, exceto os valores dos atributos <span class="codeph"> cods= </span> e <span class="codeph"> shape= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo:Públicos alvos  </span> </p> </td> 
   <td> <p>O valor de qualquer público alvo <span class="codeph">.público alvo *.label </span> e <span class="codeph">.propriedade *.userdata </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::UserData  </span> </p> </td> 
   <td> <p>O valor de qualquer propriedade. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sintaxe da cadeia de caracteres {#section-d12320edf300409f8e17565b143acafc}

Os elementos *`string`* ativados por localização no catálogo de imagens consistem em uma ou mais strings localizadas, cada uma precedida por um token de localização.

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement  </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc=  <span class="varname"> locStr  </span> ^  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId  </span> </span> </p> </td> 
  <td class="stentry"> <p>ID de localidade interna para <span class="varname"> localizedString </span> seguindo este <span class="varname"> localizationToken </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedString  </span> </span> </p> </td> 
  <td class="stentry"> <p>Sequência localizada. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString  </span> </span> </p> </td> 
  <td class="stentry"> <p>String a ser usada para localidades desconhecidas. </p> </td> 
 </tr> 
</table>

*`locId`* deve ser ASCII e não pode incluir &#39;^&#39;.

&#39;^&#39; pode ocorrer em qualquer lugar em substrings com ou sem codificação HTTP. O servidor corresponde o padrão inteiro *`localizationToken`* `^loc=locId^` a subsequências separadas.

*`stringElements`* que não incluam pelo menos um não  *`localizationToken`* sejam considerados para localização.

## O mapa de tradução {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` define as regras usadas pelo servidor para determinar qual  *`localizedStrings`* retornar ao cliente. Consiste em uma lista de entrada *`locales`* (correspondendo aos valores especificados com `locale=`), cada uma com nenhuma ou mais IDs de localidade internas ( *`locId`*). Por exemplo:

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

Valores vazios *`locId`* indicam que *`defaultString`* devem ser retornados, se disponíveis.

Consulte a descrição de `attribute::LocaleStrMap` para obter detalhes.

## O processo de tradução {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

Dado o mapa de tradução de exemplo acima e a solicitação `/is/image/myCat/myItem?req=&locale=nl`, o servidor procura primeiro &quot; `nl`&quot; no mapa de localidades. A entrada correspondente `nl,N` indica que para cada *`stringElement`*, *`localizedString`* marcado com `^loc=N^` deve ser retornado. Se *`localizationToken`* não estiver presente em *`stringElement`*, um valor vazio será retornado.

Digamos que `catalog::UserData` para `myCat/myItem` contenha o seguinte (quebras de linha inseridas para maior clareza):

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

O servidor retornaria o seguinte em resposta à nossa solicitação de exemplo:

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## Códigos de idioma desconhecidos {#section-26dfeefbd60345de94bbfeaaf7741223}

No exemplo acima, `attribute::LocaleStrMap` tem uma entrada com um valor *`locale`* vazio. O servidor usa essa entrada para manipular todos os valores `locale=` que não são explicitamente especificados de outra forma no mapa de tradução.

O mapa de tradução de exemplo especifica que, nesse caso, *`defaultString`* deve ser retornado, se disponível. Assim, o seguinte seria retornado se esse mapa de tradução fosse aplicado à solicitação `/is/image/myCat/myItem?req=&locale=ja`:

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## Exemplos {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**Famílias de línguas**

Vários valores *`locId`* podem ser associados a cada *`locale`* no mapa de conversão. Isso permite suportar variações específicas do país ou de região (por exemplo, inglês dos EUA vs inglês do Reino Unido) para selecionar *`stringElements`* enquanto lida com a maioria dos conteúdos com localidades de base comuns (por exemplo, inglês internacional).

Para o nosso exemplo, queremos adicionar suporte para inglês específico dos EUA ( ` *`locId`* EUS`) e inglês específico do Reino Unido ( ` *`locId`* EUK`), para suportar a ortografia alternativa ocasional. Se a EUK ou a EUS não existissem, voltaríamos para a E. Da mesma forma, as variantes alemãs específicas da Áustria ( `DAT`) poderiam ser disponibilizadas quando necessário, ao devolver o alemão comum *`localizedStrings`* (marcado com `D`) a maior parte do tempo.

`attribute::LocaleStrMap` se pareceria com isto:

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

A tabela a seguir descreve a saída de algumas combinações *`stringElement`* e *`locale`* representativas:

<table id="table_A6B67587C5F44B5E9CD0E7ED29A81198"> 
 <thead> 
  <tr> 
   <th class="entry"> <i>stringElement</i> </th> 
   <th class="entry"> <i>locale</i> </th> 
   <th class="entry"> <p>Sequência de saída </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^Inglês^loc=D^Alemão  </span> </p> </td> 
   <td> <p> en, en_us, en_uk </p> <p> de, de_at, de_de </p> <p>todos os outros </p> </td> 
   <td> <p>Inglês </p> <p>Alemão </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^Inglês^loc=UKE^UK-English^loc=D^Alemão^loc=DAT^Austríaco  </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>todos os outros </p> </td> 
   <td> <p>Inglês </p> <p>Reino Unido - Inglês </p> <p>Alemão </p> <p>austríaca </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch  </span> </p> <p> Observe que, neste exemplo, o <span class="varname"> locId </span> DDE não existe no atributo <span class="codeph">::LocaleStrMap </span> e, portanto, a subsequência de caracteres associada a este <span class="varname"> locId </span> nunca é retornada. </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>todos os outros </p> </td> 
   <td> <p>Inglês </p> <p>Inglês dos EUA </p> <p>Alemão </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>

