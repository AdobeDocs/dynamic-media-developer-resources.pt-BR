---
description: Mapa de tradução de cadeia de caracteres. Refere-se a um locId que pode ser mapeado para qualquer número de internalLocId.
solution: Experience Manager
title: LocaleStrMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48a1c71c-78a9-43db-8b1a-4189d34b0982
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '234'
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
  <td class="stentry"> <p> LocId <span class="varname"> </span> </p> </td> 
  <td class="stentry"> <p>ID de localidade interna. </p> </td> 
 </tr> 
</table>

`LocaleStrMap` refere-se a um `locId` que pode ser mapeado para qualquer número de `internalLocId`.

Um valor *`locale`* vazio corresponde a `locale=` cadeias de caracteres vazias e desconhecidas. Isso permite definir uma regra padrão para localidades desconhecidas.

São permitidos valores *`locId`* vazios e selecione *`defaultString`* (o *`defaultString`* não tem um identificador de localidade). *`locId`* valores são pesquisados na ordem especificada. A primeira correspondência é retornada.

A tradução de cadeias de caracteres, quando ativada, é aplicada às cadeias de texto nos seguintes campos do catálogo de imagens:

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>Campo do catálogo</b> </td> 
   <td> <b>Elemento de Cadeia de Caracteres no Campo</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::ImageSet </span> </p> </td> 
   <td> <p>Qualquer subelemento que contenha uma string traduzível (delimitada por qualquer combinação de separadores ',' ';' ':' e/ou o início/fim do campo). </p> <p>Um valor de cor <span class="codeph"> 0xrggbb </span> no início de um campo localizável é excluído da localização e passado sem modificação. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::Mapa </span> </p> </td> 
   <td> <p>Qualquer valor de atributo entre aspas simples ou duplas, exceto os valores dos atributos <span class="codeph"> coords= </span> e <span class="codeph"> shape= </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::Destinos </span> </p> </td> 
   <td> <p>O valor de qualquer destino <span class="filepath">.*.label </span> e <span class="filepath"> target.Propriedade *.userdata </span>. </p> </td> 
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

Suporte à Localização, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [catalog::Targets](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), [catalog::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
