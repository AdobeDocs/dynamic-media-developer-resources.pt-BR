---
title: Amostras.enabledragging
description: Amostras.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 6ae18f94-7a0f-429e-9684-eff43f523b1d
TQID: 'https://experienceleague.adobe.com/B50ZtREOI7H42cCjZarL4X3tO-jVSh0mXgzm3yLOzkQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 80
ht-degree: 2%

---

# Amostras.enabledragging{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

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

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enabledragging=0`
