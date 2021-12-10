---
title: ZoomView.fmt
description: ZoomView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: b46daa2f-d565-4502-8842-2b95303a77d2
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 1%

---

# ZoomView.fmt{#zoomview-fmt}

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Especifica o formato de imagem que o componente usa para carregar imagens do Servidor de imagem. Se o formato especificado terminar com <span class="codeph"> -alfa</span>, o componente renderiza imagens como conteúdo transparente. Para todos os outros formatos de imagem, o componente trata as imagens como opacas. Por padrão, o componente tem um fundo branco. Portanto, para torná-lo transparente, defina a variável <span class="codeph"> cor do fundo</span> Propriedade CSS para <span class="codeph"> transparente</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha`
