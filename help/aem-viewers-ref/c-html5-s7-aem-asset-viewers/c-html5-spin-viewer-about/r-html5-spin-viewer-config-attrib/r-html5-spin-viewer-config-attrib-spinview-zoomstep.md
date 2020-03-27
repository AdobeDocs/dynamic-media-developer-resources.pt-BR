---
description: nulo
seo-description: nulo
seo-title: SpinView.zoomstep
solution: Experience Manager
title: SpinView.zoomstep
topic: Dynamic media
uuid: f8369636-08e9-4f00-8562-86a2a907b4fa
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.zoomstep{#spinview-zoomstep}

` [SpinView.|<containerId>_spinView.]zoomstep= *``*[, *`steplimit`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> passo</span></span> </p> </td> 
   <td colname="col2"> <p> Configura as ações de aumentar e diminuir o zoom do número necessárias para aumentar ou diminuir a resolução em um fator de dois. A alteração de resolução para cada ação de zoom é de 2^1 por etapa. Defina como <span class="codeph"> 0</span> para aplicar zoom em resolução total com uma única ação de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> limite</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica a resolução máxima de zoom, relativa à imagem de resolução total. O padrão é <span class="codeph"> 1.0</span>, o que não permite o zoom além da resolução total. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Padrão {#section-7a2128fd488941948aff18421f533ccf}

`1,1`

## Example {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`zoomstep=2,3`
