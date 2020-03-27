---
description: Mapa de tradução de cadeia de caracteres. Refere-se a um locId que pode ser mapeado para qualquer número de internalLocId.
seo-description: Mapa de tradução de cadeia de caracteres. Refere-se a um locId que pode ser mapeado para qualquer número de internalLocId.
seo-title: LocaleStrMap
solution: Experience Manager
title: LocaleStrMap
topic: Scene7 Image Serving - Image Rendering API
uuid: 44207916-80a6-42cb-8bf1-fcf0f5194c6d
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# LocaleStrMap{#localestrmap}

Mapa de tradução de cadeia de caracteres. Refere-se a um locId que pode ser mapeado para qualquer número de internalLocId.

` *`item`*&#42;['|' *`item`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> locale </span>, <span class="varname"> locId </span>*[',' <span class="varname"> locId </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locale </span> </p> </td> 
  <td class="stentry"> <p>Localidade (não diferencia maiúsculas de minúsculas). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId </span> </p> </td> 
  <td class="stentry"> <p>ID de localidade interna. </p> </td> 
 </tr> 
</table>

`LocaleStrMap` refere-se a um `locId` que pode ser mapeado para qualquer número de `internalLocId`.

Um *`locale`* valor vazio corresponde a `locale=` sequências de caracteres vazias e desconhecidas. Isso permite definir uma regra padrão para localidades desconhecidas.

Valores vazios são permitidos e selecionam *`locId`* (o identificador *`defaultString`* *`defaultString`* não tem um identificador de localidade). *`locId`* são pesquisados na ordem especificada. A primeira correspondência é retornada.

A tradução de sequência de caracteres, quando ativada, é aplicada às strings de texto nos seguintes campos do catálogo de imagens:

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>Campo de catálogo</b> </td> 
   <td> <b>Elemento de string no campo</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::ImageSet </span> </p> </td> 
   <td> <p>Qualquer subelemento que contenha uma string traduzível (delimitada por qualquer combinação de separadores ',' ';' ':' e/ou o start/fim do campo). </p> <p>Um valor de <span class="codeph"> cor </span> 0xrrggbb no início de um campo localizável é excluído da localização e passado sem modificação. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::Mapa </span> </p> </td> 
   <td> <p>Qualquer valor de atributo entre aspas simples ou duplos, exceto os valores dos atributos <span class="codeph"> cords= </span> e <span class="codeph"> shape= </span> . </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo:Públicos alvos </span> </p> </td> 
   <td> <p>O valor de qualquer <span class="filepath"> público alvo.*.rótulo </span> e <span class="filepath"> público alvo.*.userdata </span> . </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::UserData </span> </p> </td> 
   <td> <p>O valor de qualquer propriedade. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-8505a8525f6948ada3979f68c4081044}

Um ou mais itens, separados por|, em que cada item consiste em dois ou mais valores separados por vírgulas, de string.

## Consulte também {#section-0c0516e4f83d42d38247308cab9b6708}

Suporte de Localização, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [atributo::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [catálogo::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [catálogo::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [catálogo::Públicos alvos](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md)[, catálogo::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
