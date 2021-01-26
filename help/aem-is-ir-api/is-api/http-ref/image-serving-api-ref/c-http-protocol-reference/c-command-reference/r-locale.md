---
description: Id Da Localidade Da Tradução. Especifica a ID de localidade para a solicitação.
seo-description: Id Da Localidade Da Tradução. Especifica a ID de localidade para a solicitação.
seo-title: locale
solution: Experience Manager
title: locale
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 82acc0bb-fd94-44c9-8ff9-3b9cefab4627
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# locale{#locale}

Id Da Localidade Da Tradução. Especifica a ID de localidade para a solicitação.

`locale=[ *`locId`*]`

<table id="simpletable_C1899AD02C984ED3896B7620916637E7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> locId</span></span> </p> </td> 
  <td class="stentry"> <p>ID da localidade (string). </p></td> 
 </tr> 
</table>

Usando essa id e as regras especificadas com `attribute::LocaleMap` e `attribute::LocaleStrMap`, o Serviço de Imagens aplica a tradução opcional da ID do catálogo e a localização da string.

## Propriedades {#section-1854a9902b884d9b8e8e713b6635723f}

comando Solicitar. Aplica-se a toda a solicitação, incluindo solicitações aninhadas/incorporadas, independentemente de onde ela seja especificada. `locId` deve incluir somente caracteres ASCII imprimíveis. Ignorado se nenhum mapa de localização estiver definido no catálogo principal desta solicitação. Um erro será retornado se `locId` for especificado vazio ou inválido e nenhuma regra padrão for definida em `attribute::DefaultLocale`.

## Padrão {#section-9699fbc26de6453e9029e0003c79a7ef}

`attribute::DefaultLocale` é usado quando locale= não é especificado.

## Consulte também {#section-28a586d43ac4429d98e318a580c92af4}

[atributo::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b) ,  [atributo::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318),  [atributo::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e), Suporte à Localização
