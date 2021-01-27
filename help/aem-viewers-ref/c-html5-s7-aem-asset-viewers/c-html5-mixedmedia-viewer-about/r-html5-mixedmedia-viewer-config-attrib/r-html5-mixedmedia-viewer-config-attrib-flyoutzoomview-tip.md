---
description: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
topic: Dynamic Media
uuid: 16a0ca99-1ed5-4f1d-b068-55adc46fde0b
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 1%

---


# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *``*[, *``*][, *`durationcountfade`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> duração</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o número de segundos em que o texto da dica é exibido antes de ser ocultado. Quando definida como <span class="codeph"> -1</span>, a mensagem será sempre exibida, mesmo se o usuário ativar o flyout. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> count</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o número de vezes que o texto é exibido ao exibir novas imagens no conjunto. Um valor de <span class="codeph"> -1</span> significa que o texto é sempre exibido ao exibir qualquer imagem no conjunto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> desvanecer</span></span> </p> </td> 
   <td colname="col2"> Especifica a duração de uma animação de esmaecimento que ocorre quando o texto é exibido ou desaparece. Um valor de <span class="codeph"> 0</span> indica que não há transição de desaparecimento. </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`3,1,0.3`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`tip=1,-1,0`
