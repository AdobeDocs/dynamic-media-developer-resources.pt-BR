---
title: zoomMode
description: Define o tipo de interação de zoom.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---

# zoomMode{#zoommode}

Define o tipo de interação de zoom.

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contínuo|inline|auto </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> contínuo </span> ativa o zoom clássico, onde a imagem é ampliada gradualmente à medida que você clica, toca duas vezes ou pinça para fora na exibição principal. Para voltar à visualização inicial, diminua o zoom ou redefina o estado do zoom. A classe </p> <p> <span class="codeph"> inline </span> ativa o zoom instantâneo, onde a imagem com zoom aparece instantaneamente ao passar o mouse sobre a exibição principal no desktop ou para tocar e segurar em um dispositivo de toque. A imagem é revertida automaticamente para o estado inicial depois que você move o mouse da exibição ou solta o dedo. Em <span class="codeph"> inline </span> , os conjuntos de imagens aninhados são nivelados e exibidos como miniaturas individuais. A classe <span class="codeph"> auto </span> ativa o modo em linha no desktop e o modo contínuo em dispositivos de toque. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
