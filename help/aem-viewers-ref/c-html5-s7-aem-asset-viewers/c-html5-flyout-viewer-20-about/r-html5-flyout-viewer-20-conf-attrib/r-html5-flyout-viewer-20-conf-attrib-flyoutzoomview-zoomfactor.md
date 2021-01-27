---
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
topic: Dynamic Media
uuid: 58d49de7-4828-46ae-b2e7-eb9398e98a99
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---


# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *``*[,[ *``*][, *`PrimaryFactorsecundárioFactorupscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> PrimaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica a ampliação da imagem para a visualização flyout, em relação à visualização principal. Deve ser um número inteiro ou um valor de ponto flutuante <span class="codeph"> 1.0</span> ou maior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Um fator secundário opcional pode ser especificado, que pode ser acessado clicando ou tocando na visualização principal quando o realce está ativo. Clicar ou tocar uma segunda vez reverte para o fator de zoom primário. Um valor de <span class="codeph"> -1</span> desativa o fator de zoom secundário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> escala</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica como o componente trata imagens pequenas. </p> <p>Se definido como <span class="codeph"> 1</span>, o componente atualiza a imagem principal para que se ajuste dentro da visualização principal. Além disso, ele atualiza a imagem de zoom para que ela preencha completamente a área da janela de flyout configurada. </p> <p>Se definido como <span class="codeph"> 0</span> imagens pequenas são exibidas na resolução original e são exibidas centralizadas na área de visualização principal e dentro da janela de flyout. Você pode configurar um espaço em branco extra que aparece ao redor da imagem com uma propriedade CSS ou de plano de fundo semelhante das classes <span class="codeph"> s7flyoutzoomview</span> e <span class="codeph"> s7flyoutzoom</span> CSS na visualização principal e na janela flyout, respectivamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Padrão {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## Exemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`
