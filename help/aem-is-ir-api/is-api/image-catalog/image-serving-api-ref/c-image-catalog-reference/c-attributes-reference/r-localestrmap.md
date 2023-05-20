---
description: Mapa de tradução de cadeia de caracteres. Refere-se a um locId que pode ser mapeado para qualquer número de internalLocId.
solution: Experience Manager
title: LocaleStrMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48a1c71c-78a9-43db-8b1a-4189d34b0982
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# LocaleStrMap{#localestrmap}

Mapa de tradução de cadeia de caracteres. Refere-se a um locId que pode ser mapeado para qualquer número de internalLocId.

`*`item`*&#42;['|' *`item`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> localidade </span>, <span class="varname"> locId </span>*[',' <span class="varname"> locId </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> localidade </span> </p> </td> 
  <td class="stentry"> <p>Local (não diferencia maiúsculas de minúsculas). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId </span> </p> </td> 
  <td class="stentry"> <p>ID de localidade interna. </p> </td> 
 </tr> 
</table>

`LocaleStrMap` refere-se a um `locId` que pode ser mapeado para qualquer número de `internalLocId`.

Um vazio *`locale`* o valor corresponde a vazio e desconhecido `locale=` strings. Isso permite definir uma regra padrão para localidades desconhecidas.

Empty *`locId`* valores são permitidos e selecione a variável *`defaultString`* (o *`defaultString`* não tem um identificador de localidade). *`locId`* Os valores são pesquisados na ordem especificada. A primeira correspondência é retornada.

A tradução de cadeias de caracteres, quando ativada, é aplicada às cadeias de texto nos seguintes campos do catálogo de imagens:

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>Campo Catálogo</b> </td> 
   <td> <b>Elemento de string no campo</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::ImageSet </span> </p> </td> 
   <td> <p>Qualquer subelemento que contenha uma string traduzível (delimitada por qualquer combinação de separadores ',' ';' ':' e/ou o início/fim do campo). </p> <p>A <span class="codeph"> 0xrrggbb </span> o valor da cor no início de um campo localizável é excluído da localização e transmitido sem modificação. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::Mapa </span> </p> </td> 
   <td> <p>Qualquer valor de atributo entre aspas simples ou duplas, exceto os valores de <span class="codeph"> coords= </span> e <span class="codeph"> forma= </span> atributos. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::Públicos-alvo </span> </p> </td> 
   <td> <p>O valor de qualquer <span class="filepath"> público-alvo.*.label </span> e <span class="filepath"> público-alvo.*.userdata </span> propriedade. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::UserData </span> </p> </td> 
   <td> <p>O valor de qualquer propriedade. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-8505a8525f6948ada3979f68c4081044}

Um ou mais itens, separados por |, quando cada item consistir em dois ou mais valores de sequência, separados por vírgulas.

## Consulte também {#section-0c0516e4f83d42d38247308cab9b6708}

Suporte à localização, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [catálogo::Mapa](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [catálogo::Públicos-alvo](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), [catálogo::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
