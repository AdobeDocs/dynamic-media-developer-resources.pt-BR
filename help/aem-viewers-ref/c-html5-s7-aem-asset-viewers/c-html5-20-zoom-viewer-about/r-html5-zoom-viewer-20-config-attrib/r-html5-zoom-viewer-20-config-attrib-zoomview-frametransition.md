---
title: ZoomView.frametransition
description: ZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f57a8a2e-63a1-4a59-9a25-b435d0ac39dc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '99'
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
