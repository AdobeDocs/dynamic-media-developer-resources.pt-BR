---
title: FlyoutZoomView.fmt
description: FlyoutZoomView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 6a9a5530-dbde-4090-8545-36bbd7322927
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 1%

---

# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_12B0B59D83BC40FCB957F41B331A1EF9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Especifica o formato de imagem a ser usado pelo componente para carregar imagens do Servidor de imagem. Se o formato especificado terminar com <span class="codeph"> -alfa</span>, o componente renderiza imagens como conteúdo transparente. Para todos os outros formatos de imagem, o componente trata as imagens como opacas. </p> <p>Por padrão, o componente tem um fundo branco. Portanto, para torná-lo transparente, defina a variável <span class="codeph"> cor do fundo</span> Propriedade CSS para <span class="codeph"> transparente</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-e6310c8c4e8547689a5b48ceddb3671d}

Opcional.

## Padrão {#section-fcb06fd8e7e945e590094efcf9a1d510}

`jpeg`

## Exemplo {#section-3a188ab955c445bcb2efa3c49722c10d}

`fmt=png-alpha`
