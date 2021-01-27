---
description: ZoomView.zoomstep
solution: Experience Manager
title: ZoomView.zoomstep
topic: Dynamic Media
uuid: 948b154a-250c-41a8-967b-d199ddb6e5e1
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 1%

---


# ZoomView.zoomstep{#zoomview-zoomstep}

` [ZoomView.|<containerId>_zoomView.]zoomstep= *``*[, *`steplimit`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> passo</span> </span> </p> </td> 
   <td colname="col2"> <p> Configura o número de ações de aumentar e diminuir o zoom necessárias para aumentar ou diminuir a resolução em um fator de dois. A alteração de resolução para cada ação de zoom é de 2^1 por etapa. Defina como <span class="codeph"> 0</span> para aplicar zoom em resolução total com uma única ação de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> limite</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica a resolução máxima de zoom, relativa à imagem de resolução total. O padrão é <span class="codeph"> 1.0</span>, o que não permite o zoom além da resolução total. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-50bcd15223174bb79ce08b31ea03d682}

Opcional.

## Padrão {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1`

## Exemplo {#section-96e69b70365f461dae4399e49044ea2f}

`zoomstep=2,3`
