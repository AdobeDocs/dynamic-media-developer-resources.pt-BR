---
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
uuid: 58d49de7-4828-46ae-b2e7-eb9398e98a99
feature: Dynamic Media Classic,Visualizadores,SDK/API,Flyout
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---


# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *``*[,[ *``*][, *`primaryFactorsecondaryFactorupscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica a ampliação de imagem para a exibição do flyout, em relação à exibição principal. Deve ser um valor inteiro ou de ponto flutuante <span class="codeph"> 1.0</span> ou maior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secundárioFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Um fator secundário opcional pode ser especificado, acessível clicando ou tocando na exibição principal quando o destaque está ativo. Clicar ou tocar uma segunda vez reverte para o fator de zoom principal. Um valor de <span class="codeph"> -1</span> desativa o fator de zoom secundário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> expansão</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica como o componente trata imagens pequenas. </p> <p>Se definido como <span class="codeph"> 1</span> o componente atualiza a imagem principal de modo a ajustá-la à exibição principal. Além disso, ele atualiza a imagem de zoom para que ela preencha completamente a área da janela do flyout configurada. </p> <p>Se definido como <span class="codeph"> 0</span> imagens pequenas são exibidas na resolução original e são exibidas centradas na área de exibição principal e dentro da janela de flyout. Você pode configurar um espaço em branco extra que aparece ao redor da imagem com uma propriedade CSS de plano de fundo ou semelhante das classes CSS <span class="codeph"> s7flyoutzoomview</span> e <span class="codeph"> s7flyoutzoom</span> na janela de exibição principal e flyout, respectivamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Padrão {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## Exemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`
