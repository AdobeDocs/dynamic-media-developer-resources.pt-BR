---
description: nulo
seo-description: nulo
seo-title: ThumbnailGridView.maxloadradius
solution: Experience Manager
title: ThumbnailGridView.maxloadradius
topic: Dynamic media
uuid: 13ea3917-346a-47c3-a535-f771910fa1c3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ThumbnailGridView.maxloadradius{#thumbnailgridview-maxloadradius}

` [ThumbnailGridView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_D29F1F6A8EC74F42A254C823435F9493"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica o comportamento de pré-carregamento do componente. </p> <p>Quando definido como <span class="codeph"> -1</span> , as miniaturas são carregadas simultaneamente quando o componente é inicializado ou o ativo muda. </p> <p>Quando definido como <span class="codeph"> 0</span> , somente as miniaturas visíveis são carregadas. </p> <p>Definir <span class="codeph"><span class="varname"> pré-carregamento</span></span> define quantas linhas/colunas invisíveis ao redor da área visível são pré-carregadas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-a3abd04c03e14c238a07349ce50d8310}

Opcional.

## Padrão {#section-c60e81667965460cbf03378a1ab9b187}

`1`

## Example {#section-472614b59e04430490a7f16c932bce89}

`maxloadradius=0`
