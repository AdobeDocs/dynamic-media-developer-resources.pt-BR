---
description: Especifica o formato de imagem que o componente usa para carregar imagens do Servidor de imagens.
seo-description: Especifica o formato de imagem que o componente usa para carregar imagens do Servidor de imagens.
seo-title: FlyoutZoomView.fmt
solution: Experience Manager
title: FlyoutZoomView.fmt
topic: Dynamic Media
uuid: 6f6a69b4-d581-44ff-b089-ce9d0d0170bf
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---


# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

Especifica o formato de imagem que o componente usa para carregar imagens do Servidor de imagens.

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alfa|gif|gif-alfa</span> </p> </td> 
   <td colname="col2"> <p> Se o formato especificado terminar com <span class="codeph"> -alfa</span>, o componente renderizará as imagens como conteúdo transparente. Para todos os outros formatos de imagem, o componente trata as imagens como opacas. </p> <p>Observe que o componente tem um fundo branco por padrão. Portanto, para torná-la completamente transparente, defina a propriedade CSS <span class="codeph"> background-color</span> como <span class="codeph"> transparente</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
