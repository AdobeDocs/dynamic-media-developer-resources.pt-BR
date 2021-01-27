---
description: CarouselView.fmt
solution: Experience Manager
title: CarouselView.fmt
topic: Dynamic Media
uuid: deba25f3-f074-42db-b1d5-d4bf22e25773
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 1%

---


# CarouselView.fmt{#carouselview-fmt}

`[CarouselView.|<containerId>_carouselView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alfa|gif|gif-alfa</span> </p> </td> 
   <td colname="col2"> <p> Especifica o formato de imagem que o componente usa para carregar imagens do Servidor de imagens. </p> <p>Se o formato especificado terminar com <span class="codeph"> -alfa</span>, o componente renderizará as imagens como conteúdo transparente. </p> <p>Para todos os outros formatos de imagem, o componente trata as imagens como opacas. O componente tem um fundo branco por padrão. Portanto, para torná-la transparente, defina a propriedade CSS <span class="codeph"> background-color</span> como <span class="codeph"> transparente</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha`
