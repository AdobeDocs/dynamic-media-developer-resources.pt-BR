---
title: Swatches.direction
description: Swatches.direction
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 906541bc-46dd-4a7c-8ee9-eb45ec3bd340
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# Swatches.direction{#swatches-direction}

`[Swatches.|<containerId>_swatches.]direction=auto|left|right`

<table id="table_B4B930A32C0742F4932BF071B9EEA9F4"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td> <p> Especifica como as amostras são preenchidas na exibição. </p> <p> <span class="codeph"> left </span> define a ordem de preenchimento da esquerda para a direita; </p> <p> <span class="codeph"> direita </span> inverte a ordem para que a exibição seja preenchida da direita para a esquerda e de cima para baixo. </p> <p>Quando <span class="codeph"> automático </span> estiver definido, o componente aplicará <span class="codeph"> direita </span> quando localidade estiver definida como <span class="codeph"> ja </span>; caso contrário, left será usado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`auto`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`direction=right`
