---
description: ZoomView.fmt
solution: Experience Manager
title: ZoomView.fmt
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom
role: Developer,Business Practitioner
exl-id: b46daa2f-d565-4502-8842-2b95303a77d2
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 1%

---

# ZoomView.fmt{#zoomview-fmt}

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Especifica o formato de imagem que o componente usa para carregar imagens do Servidor de imagem. Se o formato especificado terminar com <span class="codeph"> -alpha</span>, o componente renderizará as imagens como conteúdo transparente. Para todos os outros formatos de imagem, o componente trata as imagens como opacas. Por padrão, o componente tem um fundo branco. Portanto, para torná-lo transparente, defina a propriedade CSS <span class="codeph"> background-color</span> para <span class="codeph"> transparente</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha`
