---
description: nulo
seo-description: nulo
seo-title: CarouselView.maxloadradius
solution: Experience Manager
title: CarouselView.maxloadradius
topic: Dynamic media
uuid: 0dcebbce-f449-4f5f-acbc-02960e1dbdba
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CarouselView.maxloadradius{#carouselview-maxloadradius}

` [CarouselView.|<containerId>_carouselView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>Especifica o comportamento de pré-carregamento do componente. </p> <p>Quando definido como <span class="codeph"> -1</span> , o componente pré-carregará todos os quadros do carrossel quando em estado ocioso. </p> <p>Quando definido como <span class="codeph"> 0</span> , o componente carrega apenas o quadro que está visível no momento, o anterior e o próximo quadro. </p> <p><span class="codeph"><span class="varname"></span></span>preloadnbrdefine quantos quadros invisíveis ao redor do quadro exibido no momento são pré-carregados quando em um estado ocioso. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`1`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=0`
