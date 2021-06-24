---
description: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom em linha
role: Developer,Business Practitioner
exl-id: df73235b-547e-4d47-aa76-1d2bd4aead9b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *``*[, *``*][, *`durationcountfade`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration</span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica o número de segundos em que o texto da dica é exibido antes de ser ocultado. Quando definida como <span class="codeph"> -1</span>, a mensagem será sempre exibida, mesmo que o usuário ative o flyout. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica o número de vezes que o texto é exibido ao visualizar novas imagens no conjunto. Um valor de <span class="codeph"> -1</span> significa que o texto é sempre exibido ao visualizar qualquer imagem no conjunto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> desaparecer</span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica a duração de uma animação de esmaecimento que ocorre quando o texto aparece ou desaparece. Um valor <span class="codeph"> 0</span> significa que não há transição de esmaecimento. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-e6310c8c4e8547689a5b48ceddb3671d}

Opcional.

## Padrão {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,1,0.3`

## Exemplo {#section-3a188ab955c445bcb2efa3c49722c10d}

`tip=1,-1,0`
