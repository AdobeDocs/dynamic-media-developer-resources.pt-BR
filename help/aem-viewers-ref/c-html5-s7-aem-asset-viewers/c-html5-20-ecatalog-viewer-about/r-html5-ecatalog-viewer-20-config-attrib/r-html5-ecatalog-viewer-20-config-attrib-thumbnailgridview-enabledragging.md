---
description: ThumbnailGridView.enabledragging
solution: Experience Manager
title: ThumbnailGridView.enabledragging
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo eletrônico
role: Developer,Business Practitioner
exl-id: e3615e82-d8f0-427e-ab32-f7d0f2b6cbf3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 2%

---

# ThumbnailGridView.enabledragging{#thumbnailgridview-enabledragging}

` [ThumbnailGridView.|<containerId>_gridView.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td> <p> Ativa ou desativa a capacidade de um usuário rolar as amostras com um mouse ou usando gestos de toque </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td> <p> Funções dentro do intervalo <span class="codeph"> 0-1 </span>. É um valor <span class="codeph"> % </span> para o movimento na direção errada da velocidade real. Se estiver definido como <span class="codeph"> 1 </span>, ele se move com o mouse. Se estiver definido como <span class="codeph"> 0 </span>, isso não permitirá que você se mova na direção errada. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-831c23dea82449bfa50fd155bea365b7}

Opcional.

## Padrão {#section-464be2db89f34516ad93f32f7783d2b0}

`1,0.5`

## Exemplo {#section-e67c8807762e471bb03d6a8fb20e19d4}

`enabledragging=0`
