---
title: SpinView.sensitivity
description: SpinView.sensitivity
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 256cffae-d284-4f46-a2dc-4618ea7eda57
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---

# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *`xSensitivity`*[, *`ySensitivity`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensitivity</span>[, <span class="varname"> ySensitivity</span>]</span> </p> </td> 
   <td colname="col2"> <p> Controla a sensibilidade da rotação horizontal e vertical executada com arrastar ou deslizar o mouse. </p> <p> <span class="codeph"> xSensitivity</span> define quantas rotações de produto horizontais completas serão feitas se o usuário arrastar o mouse horizontalmente de um lado da exibição para o outro. Por exemplo, três significa que o usuário vê três rotações completas para um gesto de arrastar completo. </p> <p>Da mesma forma, <span class="codeph"> Sensibilidade</span> controla a sensibilidade da rotação vertical. Um valor de 1 significa que um arrastar ou deslizar verticalmente completo altera o ângulo de exibição do plano de rotação mais alto para o mais baixo (ou vice-versa). </p> <p>A definição de um valor negativo para <span class="codeph"> Sensibilidade</span> inverte a direção da rotação vertical. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
