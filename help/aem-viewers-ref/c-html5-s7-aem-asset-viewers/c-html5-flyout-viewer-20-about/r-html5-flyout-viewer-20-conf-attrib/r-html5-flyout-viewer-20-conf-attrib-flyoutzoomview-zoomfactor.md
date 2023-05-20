---
title: FlyoutZoomView.zoomfactor
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 150968d2-aece-4d2a-b5a8-31b03dae25bb
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---

# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *`primaryFactor`*[,[ *`secondaryFator`*][, *`upscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica a ampliação da imagem para a exibição da imagem suspensa, em relação à exibição principal. Deve ser um valor inteiro ou de ponto flutuante <span class="codeph"> 1.0</span> ou maior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFator</span> </span> </p> </td> 
   <td colname="col2"> <p> É possível especificar um fator secundário opcional, acessível clicando ou tocando na exibição principal quando o realce estiver ativo. Clicar ou tocar uma segunda vez reverte para o fator de zoom principal. Um valor de <span class="codeph"> -1</span> desativa o fator de zoom secundário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> upscale</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica como o componente lida com imagens pequenas. </p> <p>Se definida como <span class="codeph"> 1</span> o componente aumenta a imagem principal para que ela se encaixe na exibição principal. Além disso, aumenta a imagem de zoom para que ela preencha completamente a área configurada da janela de imagem suspensa. </p> <p>Se definida como <span class="codeph"> 0</span>, imagens pequenas são exibidas em sua resolução original e são exibidas centralizadas na área de visualização principal e dentro da janela da imagem suspensa. Você pode configurar o espaço em branco extra que aparece ao redor da imagem com um plano de fundo ou propriedade CSS semelhante do <span class="codeph"> s7flyoutzoomview</span> e <span class="codeph"> s7flyoutzoom</span> Classes CSS na visualização principal e na janela da imagem suspensa, respectivamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Padrão {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## Exemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`
