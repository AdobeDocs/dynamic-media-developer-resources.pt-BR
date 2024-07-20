---
title: ZoomView.zoomstep
description: ZoomView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: bcd153f3-7a87-4e8f-825b-fc4a136de1dc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---

# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *`etapa`*[, *`limite`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> etapa</span></span> </p> </td> 
   <td colname="col2"> <p> Configura o número de ações de aumento e diminuição de zoom necessárias para aumentar ou diminuir a resolução por um fator de dois. A alteração da resolução para cada ação de zoom é de 2^1 por etapa. Defina como <span class="codeph"> 0</span> para aumentar a resolução total com uma única ação de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> limite</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica a resolução máxima de zoom, relativa à resolução de imagem máxima. O padrão é <span class="codeph"> 1.0</span>, o que não permite aplicar zoom além da resolução máxima. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`1,1`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`zoomstep=2,3`
