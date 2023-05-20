---
description: ID da localidade de tradução. Especifica a ID da localidade da solicitação.
solution: Experience Manager
title: localidade
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d937dfa5-95dd-49fd-ac23-e77e07b0642c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---

# localidade{#locale}

ID da localidade de tradução. Especifica a ID da localidade da solicitação.

`locale=[ *`locId`*]`

<table id="simpletable_C1899AD02C984ED3896B7620916637E7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> locId</span></span> </p> </td> 
  <td class="stentry"> <p>ID do local (string). </p></td> 
 </tr> 
</table>

Usar essa ID e as regras especificadas com o `attribute::LocaleMap` e `attribute::LocaleStrMap`, o Servidor de imagens aplica a tradução opcional da ID do catálogo e a localização da string.

## Propriedades {#section-1854a9902b884d9b8e8e713b6635723f}

Comando Solicitar. Aplica-se a toda a solicitação, incluindo solicitações aninhadas/incorporadas, independentemente de onde for especificada. `locId` deve incluir apenas caracteres ASCII imprimíveis. Ignorado se nenhum mapa de localização for definido no catálogo principal desta solicitação. Um erro é retornado se estiver vazio ou for inválido `locId` for especificada e nenhuma regra padrão for definida em `attribute::DefaultLocale`.

## Padrão {#section-9699fbc26de6453e9029e0003c79a7ef}

`attribute::DefaultLocale` é usado quando locale= não é especificado.

## Consulte também {#section-28a586d43ac4429d98e318a580c92af4}

[attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b) , [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e), Suporte à localização
