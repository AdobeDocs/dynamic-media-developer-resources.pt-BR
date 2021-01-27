---
description: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
topic: Dynamic Media
uuid: ad423dc7-4dd8-42d9-bf75-db8f309f6aaa
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 1%

---


# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *``*[, *``*][, *`durationcountfade`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duração</span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica o número de segundos em que o texto da dica é exibido antes de ser ocultado. Quando definida como <span class="codeph"> -1</span>, a mensagem será sempre exibida, mesmo se o usuário ativar o flyout. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica o número de vezes que o texto é exibido ao exibir novas imagens no conjunto. Um valor de <span class="codeph"> -1</span> significa que o texto é sempre exibido ao exibir qualquer imagem no conjunto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> desvanecer</span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica a duração de uma animação de esmaecimento que ocorre quando o texto é exibido ou desaparece. Um valor de <span class="codeph"> 0</span> significa que não há transição de desaparecimento. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Padrão {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,1,0.3`

## Exemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`tip=1,-1,0`
