---
title: ZoomView.frametransition
description: ZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f57a8a2e-63a1-4a59-9a25-b435d0ac39dc
TQID: 'https://experienceleague.adobe.com/bnR4MQtKYsqMEDEyJN2iFpJNLMWcsc-s9mK4XQW5qpE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 99
ht-degree: 0%

---

# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *`duração`*[, *`espaçamento`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade|slide </span> </p> </td> 
   <td colname="col2"> <p>Especifica o tipo do efeito aplicado na alteração do quadro. O atributo <span class="codeph"> none </span> significa sem transição; a alteração do quadro ocorre instantaneamente. O atributo <span class="codeph"> fade </span> significa transição cross-fade entre quadros antigos e novos. O slide </span> do atributo <span class="codeph"> ativa a transição em que o quadro antigo desaparece da exibição e o novo quadro surge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duração </span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica a duração (em segundos) de <span class="codeph"> fade </span> ou <span class="codeph"> slide </span> efeito de transição. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> espaçamento </span> </span> </p> </td> 
   <td colname="col2"> <p>O espaçamento entre os quadros adjacentes na transição do slide <span class="codeph"> </span>, tem o intervalo de <span class="codeph"> 0 </span> a <span class="codeph"> 1 </span> e é relativo à largura do componente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

Nenhum.

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
