---
description: Dimensionar imagem. Dimensiona uma imagem por fator em relação à imagem de resolução completa.
seo-description: Dimensionar imagem. Dimensiona uma imagem por fator em relação à imagem de resolução completa.
seo-title: escala
solution: Experience Manager
title: escala
topic: Scene7 Image Serving - Image Rendering API
uuid: db5bab94-e5c1-41fe-ab1b-5c62b6a798d0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# escala{#scale}

Dimensionar imagem. Dimensiona uma imagem por fator em relação à imagem de resolução completa.

`scale= *`fator`*`

<table id="simpletable_AC0974B79E064BA99C1F76461BDE808A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> fator <span class="varname"></span></span> </p> </td> 
  <td class="stentry"> <p>Fator de escala (real, &gt;0). </p></td> 
 </tr> 
</table>

## Padrão {#section-e9e53959b35844579f0f1d7721b71f8e}

Se não for especificado, a imagem será usada sem dimensionamento.

## Example {#section-d5526953d6434c58bb2388bd936c13b5}

[!DNL http://server/is/agm/myRootId/myImageId?scale=.5]
