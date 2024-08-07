---
title: ZoomView.zoomstep
description: ZoomView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ded8168e-08f7-4bc0-bb8a-624bac82759e
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---

# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *`etapa`*[, *`limite`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> etapa</span> </span> </p> </td> 
   <td colname="col2"> <p> Configura o número de ações de aumento e diminuição de zoom necessárias para aumentar ou diminuir a resolução por um fator de dois. A alteração da resolução para cada ação de zoom é de 2^1 por etapa. Defina como <span class="codeph"> 0</span> para aumentar a resolução total com uma única ação de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> limite</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica a resolução máxima de zoom, relativa à resolução de imagem máxima. O padrão é <span class="codeph"> 1.0</span>, o que não permite aplicar zoom além da resolução máxima. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-50bcd15223174bb79ce08b31ea03d682}

Opcional.

## Padrão {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1`

## Exemplo {#section-96e69b70365f461dae4399e49044ea2f}

`zoomstep=2,3`
