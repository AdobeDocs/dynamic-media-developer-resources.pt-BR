---
title: FlyoutZoomView.zoomfator
description: FlyoutZoomView.zoomfator
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 2a9d4450-a1a0-471c-86bf-105d516b0bd7
TQID: 'https://experienceleague.adobe.com/9J-cksIEU-w-jRL4PN0dklGMWCpu0c74oSMdw-AX2IQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 176
ht-degree: 0%

---

# FlyoutZoomView.zoomfator{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *`primaryFactor`*[,[ *`secondaryFactor`*][, *`upscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica a ampliação da imagem para a exibição da imagem suspensa, em relação à exibição principal. Deve ser um número inteiro ou um valor de ponto flutuante <span class="codeph"> 1.0</span> ou maior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> É possível especificar um fator secundário opcional, acessível clicando ou tocando na exibição principal quando o realce estiver ativo. Clicar ou tocar uma segunda vez reverte para o fator de zoom principal. Um valor de <span class="codeph"> -1</span> desabilita o fator de zoom secundário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> upscale</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica como o componente lida com imagens pequenas. </p> <p>Se definido como <span class="codeph"> 1</span>, o componente expande a imagem principal para que ela se ajuste à exibição principal. Além disso, aumenta a imagem de zoom para que ela preencha completamente a área configurada da janela de imagem suspensa. </p> <p>Se definido como <span class="codeph"> 0</span>, imagens pequenas são exibidas em sua resolução original e são exibidas centralizadas na área de exibição principal e dentro da janela da imagem suspensa. Você pode configurar um espaço em branco extra ao redor da imagem com uma propriedade CSS semelhante ou de plano de fundo das classes CSS <span class="codeph"> s7flyoutzoomview</span> e <span class="codeph"> s7flyoutzoom</span> na exibição principal e na janela de imagem suspensa, respectivamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-e6310c8c4e8547689a5b48ceddb3671d}

Opcional.

## Padrão {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,-1,1`

## Exemplo {#section-3a188ab955c445bcb2efa3c49722c10d}

`zoomfactor=2,3,0`
