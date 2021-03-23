---
description: SpinView.zoomstep
solution: Experience Manager
title: SpinView.zoomstep
uuid: 103097e9-7e6d-413c-a6a8-b8a15665348c
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídias mistas
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 1%

---


# SpinView.zoomstep{#spinview-zoomstep}

` [SpinView.|<containerId>_spinView.]zoomstep= *``*[, *`steplimit`*]`

<table id="table_2D7F971D503348B8A9559362A1D9B26D"> 
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

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomstep=2,3`
