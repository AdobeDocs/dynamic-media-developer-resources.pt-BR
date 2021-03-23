---
description: Define o tipo de interação de zoom.
seo-description: Define o tipo de interação de zoom.
seo-title: zoomMode
solution: Experience Manager
title: zoomMode
uuid: fdbe7ab6-47db-46cf-8a0d-085c66d4b0f8
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídias mistas
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '151'
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
