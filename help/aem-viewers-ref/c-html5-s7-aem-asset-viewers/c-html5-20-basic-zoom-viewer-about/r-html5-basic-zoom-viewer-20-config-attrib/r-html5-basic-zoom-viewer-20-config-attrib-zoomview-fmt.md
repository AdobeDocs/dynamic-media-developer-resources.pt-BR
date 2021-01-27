---
description: ZoomView.fmt
solution: Experience Manager
title: ZoomView.fmt
topic: Dynamic Media
uuid: b118e441-f128-4dfd-a82e-62ec4d1ebf84
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 1%

---


# ZoomView.fmt{#zoomview-fmt}

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alfa|gif|gif-alfa</span> </p> </td> 
   <td colname="col2"> <p> Especifica o formato de imagem que o componente usa para carregar imagens do Servidor de imagens. Se o formato especificado terminar com "-alfa ", o componente renderizará as imagens como conteúdo transparente. Para todos os outros formatos de imagem, o componente trata as imagens como opacas. O componente tem um fundo branco por padrão. Portanto, para torná-la transparente, defina a propriedade CSS de cor de fundo como transparente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-50bcd15223174bb79ce08b31ea03d682}

Opcional.

## Padrão {#section-7564169749ff4a4996049ea1148cb2a5}

`jpeg`

## Exemplo {#section-96e69b70365f461dae4399e49044ea2f}

`fmt=png-alpha`
