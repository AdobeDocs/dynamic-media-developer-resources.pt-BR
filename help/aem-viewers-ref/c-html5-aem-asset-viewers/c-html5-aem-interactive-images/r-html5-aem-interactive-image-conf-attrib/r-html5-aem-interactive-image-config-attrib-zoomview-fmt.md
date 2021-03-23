---
description: Especifica o formato de imagem que o componente usa para carregar imagens do Servidor de imagem.
seo-description: Especifica o formato de imagem que o componente usa para carregar imagens do Servidor de imagem.
seo-title: ZoomView.fmt
solution: Experience Manager
title: ZoomView.fmt
uuid: 73a2196f-0ece-497a-9a12-376dafbbae56
feature: Dynamic Media Classic,Visualizadores,SDK/API,Imagens interativas
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---


# ZoomView.fmt{#zoomview-fmt}

Especifica o formato de imagem que o componente usa para carregar imagens do Servidor de imagem.

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Se o formato especificado terminar com <span class="codeph"> -alpha</span>, o componente renderizará as imagens como conteúdo transparente. Para todos os outros formatos de imagem, o componente trata as imagens como opacas. Por padrão, o componente tem um fundo branco. Portanto, para torná-lo transparente, defina a propriedade CSS <span class="codeph"> background-color</span> para <span class="codeph"> transparente</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha`
