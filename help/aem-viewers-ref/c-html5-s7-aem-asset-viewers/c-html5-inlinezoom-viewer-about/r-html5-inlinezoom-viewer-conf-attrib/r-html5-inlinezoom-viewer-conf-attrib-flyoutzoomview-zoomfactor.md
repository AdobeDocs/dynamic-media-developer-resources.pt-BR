---
title: FlyoutZoomView.zoomfactor
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 2a9d4450-a1a0-471c-86bf-105d516b0bd7
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---

# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *`primaryFactor`*[,[ *`secundárioFactor`*][, *`expansão`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica a ampliação de imagem para a exibição do flyout, em relação à exibição principal. Deve ser um valor inteiro ou de ponto flutuante <span class="codeph"> 1,0</span> ou maior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secundárioFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Um fator secundário opcional pode ser especificado, acessível clicando ou tocando na exibição principal quando o destaque está ativo. Clicar ou tocar uma segunda vez reverte para o fator de zoom principal. Um valor de <span class="codeph"> -1</span> desativa o fator de zoom secundário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> expansão</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica como o componente trata imagens pequenas. </p> <p>Se estiver definido como <span class="codeph"> 1</span> o componente dimensiona a imagem principal de forma que se ajuste à exibição principal. Além disso, ele atualiza a imagem de zoom para que ela preencha completamente a área da janela do flyout configurada. </p> <p>Se estiver definido como <span class="codeph"> 0</span>, imagens pequenas são exibidas na resolução original e são exibidas centralizadas na área de visualização principal e dentro da janela do flyout. Você pode configurar um espaço em branco extra ao redor da imagem com um plano de fundo ou uma propriedade CSS semelhante do <span class="codeph"> s7flyoutzoomview</span> e <span class="codeph"> s7flyoutzoom</span> Classes CSS na exibição principal e na janela de flyout, respectivamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-e6310c8c4e8547689a5b48ceddb3671d}

Opcional.

## Padrão {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,-1,1`

## Exemplo {#section-3a188ab955c445bcb2efa3c49722c10d}

`zoomfactor=2,3,0`
