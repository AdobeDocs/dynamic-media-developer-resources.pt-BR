---
description: nulo
seo-description: nulo
seo-title: SpinView.sensitivity
solution: Experience Manager
title: SpinView.sensitivity
topic: Dynamic media
uuid: 82cf1f26-3af0-494f-b918-fdc318959c75
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *`Sensibilidade`*[, *`x`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensitivity</span>[,  <span class="varname"> ySensitivity</span>]</span> </p> </td> 
   <td colname="col2"> <p> Controla a sensibilidade da rotação horizontal e vertical executada com um arraste ou deslize do mouse. </p> <p> <span class="codeph"> O </span> xSensitivity define quantas rotações de produto horizontais completas são feitas se o usuário arrasta o mouse horizontalmente de um lado da visualização para o outro. Por exemplo, três significa que o usuário vê três rotações completas para um gesto de arrastar completo. </p> <p>Da mesma forma, <span class="codeph"> ySensitivity</span> controla a sensibilidade do spin vertical. Um valor de 1 significa que um arrastar ou deslizar verticalmente inteiro altera o ângulo de visualização do plano de rotação mais alto para o mais baixo (ou vice-versa). </p> <p>A definição de um valor negativo para <span class="codeph"> ySensitivity</span> inverte a direção da rotação vertical. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
