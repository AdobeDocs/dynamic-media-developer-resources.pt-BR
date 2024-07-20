---
description: ThumbnailGridView.enabledragging
solution: Experience Manager
title: ThumbnailGridView.enabledragging
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 011ef772-6760-4794-819e-2a822fbae1b5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# ThumbnailGridView.enabledragging{#thumbnailgridview-enabledragging}

[!DNL `[ThumbnailGridView.|<containerId>_gridView.]enabledragging=0|1[, *`overdragvalue`*]`]

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td> <p> Ativa ou desativa a opção de rolagem das amostras com o mouse ou com gestos de toque </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td> <p> Funções dentro do intervalo <span class="codeph"> 0-1 </span>. É um valor de <span class="codeph"> % </span> para o movimento na direção errada da velocidade real. Se estiver definido como <span class="codeph"> 1 </span>, ele se move com o mouse. Se estiver definido como <span class="codeph"> 0 </span>, ele não permite que você mova para a direção errada. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-831c23dea82449bfa50fd155bea365b7}

Opcional.

## Padrão {#section-464be2db89f34516ad93f32f7783d2b0}

[!DNL `1,0.5`]

## Exemplo {#section-e67c8807762e471bb03d6a8fb20e19d4}

[!DNL `enabledragging=0`]
