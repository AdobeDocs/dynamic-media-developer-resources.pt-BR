---
description: SpinView.zoomstep
solution: Experience Manager
title: SpinView.zoomstep
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de rotação
role: Developer,Business Practitioner
exl-id: 919477d0-87d9-4cf7-a7c8-0fbb68c6ff96
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 1%

---

# SpinView.zoomstep{#spinview-zoomstep}

` [SpinView.|<containerId>_spinView.]zoomstep= *``*[, *`steplimit`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> step</span></span> </p> </td> 
   <td colname="col2"> <p> Configura as ações de ampliação e redução de zoom numérico necessárias para aumentar ou diminuir a resolução em um fator de dois. A alteração da resolução para cada ação de zoom é de 2^1 por etapa. Defina como <span class="codeph"> 0</span> para aplicar zoom a resolução completa com uma única ação de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> limite</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica a resolução máxima de zoom, relativa à imagem de resolução completa. O padrão é <span class="codeph"> 1.0</span>, o que não permite zoom além da resolução completa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Padrão {#section-7a2128fd488941948aff18421f533ccf}

`1,1`

## Exemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`zoomstep=2,3`
