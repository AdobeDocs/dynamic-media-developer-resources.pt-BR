---
description: ThumbnailGridView.maxloadradius
solution: Experience Manager
title: ThumbnailGridView.maxloadradius
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: acbcea10-950d-4f98-be5a-5aead9f4e0d9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 0%

---

# ThumbnailGridView.maxloadradius{#thumbnailgridview-maxloadradius}

[!DNL `[ThumbnailGridView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_D29F1F6A8EC74F42A254C823435F9493"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica o comportamento do carregamento prévio do componente. </p> <p>Quando definido como <span class="codeph"> -1</span>, as miniaturas são carregadas simultaneamente quando o componente é inicializado ou o ativo muda. </p> <p>Quando definido como <span class="codeph"> 0</span>, somente as miniaturas visíveis são carregadas. </p> <p>Definir <span class="codeph"><span class="varname"> preloadnbr</span></span> define quantas linhas/colunas invisíveis em torno da área visível são pré-carregadas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-a3abd04c03e14c238a07349ce50d8310}

Opcional.

## Padrão {#section-c60e81667965460cbf03378a1ab9b187}

[!DNL `1`]

## Exemplo {#section-472614b59e04430490a7f16c932bce89}

[!DNL `maxloadradius=0`]
