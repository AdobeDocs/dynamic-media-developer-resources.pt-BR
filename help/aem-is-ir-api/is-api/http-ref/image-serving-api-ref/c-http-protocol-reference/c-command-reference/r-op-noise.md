---
description: Adicione ruído. Adiciona ruído aleatório aos dados da imagem de primeiro plano ou ao primeiro plano de uma camada de efeito.
solution: Experience Manager
title: op_sound
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---


# op_sound{#op-noise}

Adicione ruído. Adiciona ruído aleatório aos dados da imagem de primeiro plano ou ao primeiro plano de uma camada de efeito.

`op_noise= *``*[,uniform|gaussian[, *`valmonocromático`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>Quantidade de ruído em porcentagem (0...100 int). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> uniforme</span> </p> </td> 
   <td colname="col2"> <p>Selecione a distribuição uniforme de ruídos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> gaussiano</span> </p> </td> 
   <td colname="col2"> <p>Selecione gaussisian sound distribution . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> monocromático</span> </p> </td> 
   <td colname="col2"> <p>Defina como 0 para o ruído de cor, 1 para o ruído de cinza. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* é ignorado para imagens em tons de cinza.

## Propriedades {#section-1f1a64c791f545a3bf1abd0b0e575d87}

comando Camada. Aplica-se à camada atual ou à imagem composta se `layer=comp`.

## Padrão {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`, sem ruído.
