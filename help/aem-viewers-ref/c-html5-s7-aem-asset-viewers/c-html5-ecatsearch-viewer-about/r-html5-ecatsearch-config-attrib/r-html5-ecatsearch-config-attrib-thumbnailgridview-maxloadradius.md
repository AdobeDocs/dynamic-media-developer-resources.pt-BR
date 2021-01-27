---
description: ThumbnailGridView.maxloadradius
solution: Experience Manager
title: ThumbnailGridView.maxloadradius
topic: Dynamic Media
uuid: e72ae5d6-574e-4f30-827c-021ce5dafcee
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 1%

---


# ThumbnailGridView.maxloadradius{#thumbnailgridview-maxloadradius}

[!DNL `[ThumbnailGridView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_D29F1F6A8EC74F42A254C823435F9493"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica o comportamento de pré-carregamento do componente. </p> <p>Quando definido como <span class="codeph"> -1</span> as miniaturas são carregadas simultaneamente quando o componente é inicializado ou o ativo muda. </p> <p>Quando definido como <span class="codeph"> 0</span> apenas as miniaturas visíveis são carregadas. </p> <p>Definir <span class="codeph"><span class="varname"> preloadnbr</span></span> define quantas linhas/colunas invisíveis ao redor da área visível são pré-carregadas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-a3abd04c03e14c238a07349ce50d8310}

Opcional.

## Padrão {#section-c60e81667965460cbf03378a1ab9b187}

[!DNL `1`]

## Exemplo {#section-472614b59e04430490a7f16c932bce89}

[!DNL `maxloadradius=0`]
