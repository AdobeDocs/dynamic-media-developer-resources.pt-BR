---
title: FlyoutZoomView.frametransition
description: FlyoutZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 39cb629a-3940-4206-91cd-fe9a9f4d9f75
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---

# FlyoutZoomView.frametransition{#flyoutzoomview-frametransition}

` [FlyoutZoomView.|<containerId>_flyout.]frametransition=none|fade[, *`duração`*]`

<table id="table_FC34B37AACFB4E92A37E1D2D93D5F0D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nenhuma|desaparecimento</span> </p> </td> 
   <td colname="col2"> <p> </p> <p> Especifica o tipo do efeito aplicado à exibição principal na alteração do ativo. </p> <p><span class="codeph"> none</span> significa sem transição, a alteração da exibição principal acontece instantaneamente. </p> <p><span class="codeph"> fade</span> ativa a transição cross-fade onde a imagem desaparece e a nova imagem aparece </p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duração</span></span> </p> </td> 
   <td colname="col2"> <p> Número de segundos que a animação leva para terminar. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-e6310c8c4e8547689a5b48ceddb3671d}

Opcional.

## Padrão {#section-fcb06fd8e7e945e590094efcf9a1d510}

Nenhum.

## Exemplo {#section-3a188ab955c445bcb2efa3c49722c10d}

`frametransition=fade,1`
