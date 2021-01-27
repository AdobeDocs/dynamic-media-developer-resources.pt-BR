---
description: SpinView.autospin
solution: Experience Manager
title: SpinView.autospin
topic: Dynamic Media
uuid: 9d24ed39-e4b9-442b-bc64-c77707ff69d8
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 2%

---


# SpinView.autospin{#spinview-autospin}

` [SpinView.|<containerId>_spinView.]maxloadradius=0|1[, *``*][, *``*][, *`durationdirectionspin_number`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Ativa ou desativa a animação de rotação automática. Para obter a melhor experiência de rotação automática, é recomendável pré-carregar todos os quadros definindo <span class="codeph"> maxloadradius</span> como <span class="codeph"> -1</span>. Entretanto, observe que isso resulta em maior tempo de carga e maior uso da largura de banda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duração</span></span> </p> </td> 
   <td colname="col2"> <p> O número de segundos por uma rotação completa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> direção</span></span> </p> </td> 
   <td colname="col2"> <p> A direção de rotação que é <span class="codeph"> 0</span> para leste girando e <span class="codeph"> 1</span> para oeste girando. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> spin_number</span></span> </p> </td> 
   <td colname="col2"> <p> O número de rotações completas feitas antes de a rotação automática parar. O número é um número de ponto flutuante. Defina como <span class="codeph"> -1</span> para obter uma rotação automática infinita. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Padrão {#section-7a2128fd488941948aff18421f533ccf}

`0,1,1,1`

## Exemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`autospin=1,2,-1,1`
