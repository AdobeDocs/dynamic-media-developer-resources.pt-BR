---
title: ZoomView.frametransition
description: ZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f57a8a2e-63a1-4a59-9a25-b435d0ac39dc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 1%

---

# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *`duration`*[, *`espaçamento`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nenhum|esmaecer|slide </span> </p> </td> 
   <td colname="col2"> <p>Especifica o tipo de efeito aplicado na alteração de quadro. O atributo <span class="codeph"> nenhum </span> não significa transição; a mudança de quadro ocorre instantaneamente. O atributo <span class="codeph"> desaparecer </span> significa a transição entre o esmaecimento antigo e o novo quadro. O atributo <span class="codeph"> slide </span> ativa a transição, na qual o quadro antigo desliza para fora da exibição e o novo quadro desliza para dentro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration </span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica a duração (em segundos) de <span class="codeph"> desaparecer </span> ou <span class="codeph"> slide </span> efeito de transição. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> espaçamento </span> </span> </p> </td> 
   <td colname="col2"> <p>O espaçamento entre os quadros adjacentes em <span class="codeph"> slide </span> , tem o intervalo de <span class="codeph"> 0 </span> through <span class="codeph"> 1 </span> e é relativo à largura do componente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

Nenhum.

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
