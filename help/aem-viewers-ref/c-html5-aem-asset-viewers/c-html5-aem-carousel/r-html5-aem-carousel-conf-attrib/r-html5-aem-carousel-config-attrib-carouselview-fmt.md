---
description: nulo
seo-description: nulo
seo-title: CarouselView.fmt
solution: Experience Manager
title: CarouselView.fmt
topic: Dynamic media
uuid: deba25f3-f074-42db-b1d5-d4bf22e25773
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CarouselView.fmt{#carouselview-fmt}

`[CarouselView.|<containerId>_carouselView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alfa|gif|gif-alfa</span> </p> </td> 
   <td colname="col2"> <p> Especifica o formato de imagem que o componente usa para carregar imagens do Servidor de imagens. </p> <p>Se o formato especificado terminar com <span class="codeph"> -alfa</span>, o componente renderizará as imagens como conteúdo transparente. </p> <p>Para todos os outros formatos de imagem, o componente trata as imagens como opacas. O componente tem um fundo branco por padrão. Portanto, para torná-la transparente, defina a propriedade CSS de cor <span class="codeph"> de fundo como</span> transparente <span class="codeph"></span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha`
