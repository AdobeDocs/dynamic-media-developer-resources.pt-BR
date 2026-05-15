---
title: InterativeSwatches.enabledragging
description: Atributo de configuração para o Visualizador de vídeo interativo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 91c5eb52-40d9-40f6-8687-e68cb40b634e
TQID: 'https://experienceleague.adobe.com/-CG9cDCgGht0hFS3dkQVutUkrHA8ka3P263U65m-E5U'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 88
ht-degree: 2%

---

# InterativeSwatches.enabledragging{#interactiveswatches-enabledragging}

Atributo de configuração para o Visualizador de vídeo interativo.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Ativa ou desativa a opção de rolagem das amostras com o mouse ou com gestos de toque. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td colname="col2"> <p> Está no intervalo <span class="codeph"> 0-1 </span> e é um valor percentual para o movimento na direção errada da velocidade real. </p> <p>Se definido como <span class="codeph"> 1 </span>, ele se move com o mouse. </p> <p>Se definido como <span class="codeph"> 0 </span>, ele não permite que você mova para a direção errada. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
enabledragging=0
```
