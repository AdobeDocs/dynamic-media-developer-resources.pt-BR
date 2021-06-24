---
description: SpinView.autospin
solution: Experience Manager
title: SpinView.autospin
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de rotação
role: Developer,Business Practitioner
exl-id: 16276e07-5494-4fd9-bd77-e77a46c57fd1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 1%

---

# SpinView.autospin{#spinview-autospin}

` [SpinView.|<containerId>_spinView.]maxloadradius=0|1[, *``*][, *``*][, *`durationdirectionspin_number`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Ativa ou desativa a animação de rotação automática. Para obter a melhor experiência de rotação automática, é recomendável pré-carregar todos os quadros configurando <span class="codeph"> maxloadradius</span> para <span class="codeph"> -1</span>. Observe, no entanto, que isso resulta em maior tempo de carga e maior uso da largura de banda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duration</span></span> </p> </td> 
   <td colname="col2"> <p> O número de segundos por um giro completo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> direção</span></span> </p> </td> 
   <td colname="col2"> <p> A direção de rotação que é <span class="codeph"> 0</span> para girar para leste e <span class="codeph"> 1</span> para girar para oeste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> spin_number</span></span> </p> </td> 
   <td colname="col2"> <p> O número total de rotações feitas antes da interrupção da autorotação. O número é um número de ponto flutuante. Defina como <span class="codeph"> -1</span> para um giro automático infinito. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Padrão {#section-7a2128fd488941948aff18421f533ccf}

`0,1,1,1`

## Exemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`autospin=1,2,-1,1`
