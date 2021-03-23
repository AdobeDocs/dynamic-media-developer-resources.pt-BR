---
description: Mapa de tradução de cadeia de caracteres. Refere-se a um locId que pode ser mapeado para qualquer número de internalLocId.
seo-description: Mapa de tradução de cadeia de caracteres. Refere-se a um locId que pode ser mapeado para qualquer número de internalLocId.
seo-title: LocaleStrMap
solution: Experience Manager
title: LocaleStrMap
uuid: 44207916-80a6-42cb-8bf1-fcf0f5194c6d
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---


# LocaleStrMap{#localestrmap}

Mapa de tradução de cadeia de caracteres. Refere-se a um locId que pode ser mapeado para qualquer número de internalLocId.

`*``*&#42;['|' *`item`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item  </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> locale  </span>,  <span class="varname"> locId  </span>*[','  <span class="varname"> locId  </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locale  </span> </p> </td> 
  <td class="stentry"> <p>Localidade (não diferencia maiúsculas de minúsculas). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId  </span> </p> </td> 
  <td class="stentry"> <p>ID de localidade interna. </p> </td> 
 </tr> 
</table>

`LocaleStrMap` refere-se a um  `locId` que pode ser mapeado para qualquer número de  `internalLocId`.

Um valor vazio *`locale`* corresponde a sequências vazias e desconhecidas `locale=`. Isso permite definir uma regra padrão para localidades desconhecidas.

Valores vazios *`locId`* são permitidos e selecione o *`defaultString`* (o *`defaultString`* não tem um identificador de localidade). *`locId`* são pesquisados na ordem especificada. A primeira correspondência é retornada.

A tradução de sequência, quando ativada, é aplicada às sequências de texto nos seguintes campos do catálogo de imagem:

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>Campo de catálogo</b> </td> 
   <td> <b>Elemento de string no campo</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::ImageSet  </span> </p> </td> 
   <td> <p>Qualquer subelemento que contenha uma string traduzível (delimitada por qualquer combinação de separadores ',' ';' ':' e/ou o início/fim do campo). </p> <p>Um valor de cor <span class="codeph"> 0xrrggbb </span> no início de um campo localizável é excluído da localização e passado sem modificação. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::Mapa  </span> </p> </td> 
   <td> <p>Qualquer valor de atributo entre aspas simples ou duplas, exceto os valores dos atributos <span class="codeph"> e </span> shape= </span>.<span class="codeph"> </span></p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::Metas  </span> </p> </td> 
   <td> <p>O valor de qualquer destino <span class="filepath">.*.label </span> e <span class="filepath"> target.propriedade *.userdata </span> . </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::UserData  </span> </p> </td> 
   <td> <p>O valor de qualquer propriedade. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-8505a8525f6948ada3979f68c4081044}

Um ou mais itens, separados por |, em que cada item consiste de dois ou mais valores de string separados por vírgulas.

## Consulte também {#section-0c0516e4f83d42d38247308cab9b6708}

Suporte de localização, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [atributo::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [catálogo::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [catálogo::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [catálogo::Targets](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), [catálogo::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
