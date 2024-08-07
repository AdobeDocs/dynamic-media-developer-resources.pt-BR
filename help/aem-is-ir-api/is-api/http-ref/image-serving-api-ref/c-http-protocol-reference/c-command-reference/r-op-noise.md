---
title: op_noise
description: Adicione ruído. Adiciona ruído aleatório aos dados da imagem de primeiro plano ou ao primeiro plano de uma camada de efeito.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eeadd3ab-80ff-4f9b-b5b7-4f3da6feebde
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# op_noise{#op-noise}

Adicione ruído. Adiciona ruído aleatório aos dados da imagem de primeiro plano ou ao primeiro plano de uma camada de efeito.

`op_noise= *`val`*[,uniform|gaussian[, *`monocromático`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>Quantidade de ruído em porcentagem (0 a 100 int). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> uniforme</span> </p> </td> 
   <td colname="col2"> <p>Selecione Uniforme Noise Distribution (Distribuição uniforme de ruído). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> gaussiano</span> </p> </td> 
   <td colname="col2"> <p>Selecione a distribuição de ruído gaussiano. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> monocromático</span> </p> </td> 
   <td colname="col2"> <p>Defina como 0 para ruído de cor, 1 para ruído cinza. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* é ignorado para imagens em tons de cinza.

## Propriedades {#section-1f1a64c791f545a3bf1abd0b0e575d87}

Camada. Aplica-se à camada atual ou à imagem composta, se `layer=comp`.

## Padrão {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`, sem ruído.
