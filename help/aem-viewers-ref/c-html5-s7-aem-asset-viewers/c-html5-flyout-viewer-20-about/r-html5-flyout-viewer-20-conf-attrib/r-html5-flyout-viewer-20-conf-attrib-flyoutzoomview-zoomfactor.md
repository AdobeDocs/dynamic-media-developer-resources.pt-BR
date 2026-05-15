---
title: FlyoutZoomView.zoomfator
description: FlyoutZoomView.zoomfator
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 150968d2-aece-4d2a-b5a8-31b03dae25bb
TQID: 'https://experienceleague.adobe.com/Zp4VYoGBfivwXRZQ7dmtouoy2qFMZePQKDrocHaBPXk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 178
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
   <td colname="col2"> <p>Especifica como o componente lida com imagens pequenas. </p> <p>Se definido como <span class="codeph"> 1</span>, o componente expande a imagem principal para que ela se ajuste à exibição principal. Além disso, aumenta a imagem de zoom para que ela preencha completamente a área configurada da janela de imagem suspensa. </p> <p>Se definido como <span class="codeph"> 0</span>, imagens pequenas são exibidas em sua resolução original e são exibidas centralizadas na área de exibição principal e dentro da janela da imagem suspensa. Você pode configurar um espaço em branco extra que apareça ao redor da imagem com uma propriedade CSS semelhante ou de plano de fundo das classes CSS <span class="codeph"> s7flyoutzoomview</span> e <span class="codeph"> s7flyoutzoom</span> na exibição principal e na janela de imagem suspensa, respectivamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Padrão {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## Exemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`
