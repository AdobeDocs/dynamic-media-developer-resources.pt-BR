---
description: Define o tipo de interação de zoom.
solution: Experience Manager
title: zoomMode
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídia mista
role: Developer,User
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# zoomMode{#zoommode}

Define o tipo de interação de zoom.

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contínuo|inline|auto  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> o contínuo  </span> permite o zoom clássico, onde a imagem é gradualmente ampliada à medida que você clica, toca duas vezes ou pinça na exibição principal. Você precisa diminuir o zoom explicitamente ou redefinir o estado do zoom para voltar à visualização inicial. </p> <p> <span class="codeph"> em linha  </span> permite o zoom instantâneo, onde a imagem com zoom aparece instantaneamente ao passar o mouse sobre a exibição principal no desktop ou tocar e segurar em um dispositivo de toque; A imagem é revertida automaticamente para o estado inicial assim que você move o mouse da exibição ou solta o dedo. Observe que no modo <span class="codeph"> em linha </span> os conjuntos de imagens aninhados são nivelados e exibidos como miniaturas individuais. <span class="codeph"> O  </span> ativa o modo em linha no desktop e o modo contínuo em dispositivos de toque. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
