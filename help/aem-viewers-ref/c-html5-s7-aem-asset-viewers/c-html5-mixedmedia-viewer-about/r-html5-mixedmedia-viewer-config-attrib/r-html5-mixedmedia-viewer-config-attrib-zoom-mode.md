---
description: Define o tipo de interação de zoom.
seo-description: Define o tipo de interação de zoom.
seo-title: zoomMode
solution: Experience Manager
title: zoomMode
topic: Dynamic Media
uuid: fdbe7ab6-47db-46cf-8a0d-085c66d4b0f8
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---


# zoomMode{#zoommode}

Define o tipo de interação de zoom.

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contínuo|inline|automático  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> contínuo  </span> permite o zoom clássico no qual a imagem é gradualmente ampliada ao clicar, tocar no duplo ou afastar o dedo na visualização principal. É necessário diminuir explicitamente o zoom ou redefinir o estado de zoom para voltar à visualização inicial. </p> <p> <span class="codeph"> em linha  </span> permite o zoom instantâneo, em que a imagem ampliada aparece instantaneamente quando você passa o mouse sobre a visualização principal no desktop ou para tocar e segurar em um dispositivo de toque; a imagem reverte automaticamente para o estado inicial quando você move o mouse da visualização ou solta o dedo. Observe que no modo <span class="codeph"> inline </span> os conjuntos de imagens aninhados são nivelados e exibidos como miniaturas individuais. <span class="codeph"> auto  </span> ativa o modo em linha na área de trabalho e o modo contínuo nos dispositivos de toque. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
