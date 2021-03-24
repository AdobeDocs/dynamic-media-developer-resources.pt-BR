---
description: SpinView.sensitivity
solution: Experience Manager
title: SpinView.sensitivity
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de rotação
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# SpinView.sensitivity{#spinview-sensitivity}

` [SpinView.|<containerId>_spinView.]sensitivity= *``*[, *`xSensibilidade`*]`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> xSensibilidade</span>[,  <span class="varname"> Sensibilidade</span>]</span> </p> </td> 
   <td colname="col2"> <p> Controla a sensibilidade da rotação horizontal e vertical executada com um arrastar ou deslizar o mouse. </p> <p> <span class="codeph"> </span> xSensibilidade define quantas rotações de produto horizontais completas são feitas se o usuário arrastar o mouse horizontalmente de um lado da exibição para o outro. Por exemplo, três significa que o usuário vê três rotação completa para um gesto de arrastar completo. </p> <p>Da mesma forma, <span class="codeph"> Sensibilidade</span> controla a sensibilidade do giro vertical. Um valor de 1 significa que um arrastar ou deslizar vertical total altera o ângulo de exibição do plano de rotação mais alto para o mais inferior (ou vice-versa). </p> <p>Definir um valor negativo para <span class="codeph"> Sensibilidade</span> inverte a direção do eixo vertical. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`5,2`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`sensitivity=4,-2`
