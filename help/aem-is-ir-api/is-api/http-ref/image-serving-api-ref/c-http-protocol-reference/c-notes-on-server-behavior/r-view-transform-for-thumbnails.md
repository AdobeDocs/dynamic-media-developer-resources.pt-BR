---
description: A imagem retornada ao cliente em resposta a uma solicitação req=tmb é derivada da imagem composta considerando os seguintes valores wid=, hei=, atributo DefaultThumbPix e atributo MaxPix.
solution: Experience Manager
title: Exibir transformação para miniaturas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# Exibir transformação para miniaturas{#view-transform-for-thumbnails}

A imagem retornada ao cliente em resposta a uma solicitação req=tmb é derivada da imagem composta considerando os seguintes valores: wid=, hei=, atributo::DefaultThumbPix e atributo::MaxPix.

1. **Calcular o valor da exibição** - Uso `wid=` ou o valor de largura de `attribute::DefaultThumbPix` para a largura do direito de exibição. Use `hei=` ou o valor da altura de `attribute::DefaultThumbPix` para a altura. O direito de exibição deve ser totalmente especificado nesta etapa. (Observe que o reto de exibição é o mesmo da camada 0, se não `size=`é especificado para a camada 0).
1. **Dimensionar o composto** - If `catalog::ThumbType=Crop`, o compósito é dimensionado para a menor imagem possível enquanto ainda preenche todo o gráfico de visualização; os dados de imagem extras são cortados. If `catalog::ThumbType= Fit`, o compósito é dimensionado para a maior imagem possível enquanto ainda ajusta todo o compósito para o retângulo de exibição. If `catalog::ThumbType=Texture`, o composto não é dimensionado de forma alguma para preservar a resolução especificada em `catalog::ThumbRes`.
1. **Preencher e cortar** - O gráfico de exibição é preenchido com a variável `bgc=` cor (ou, se não especificado, com `attribute::ThumbBkgColor`). O composto dimensionado é alinhado com o direito de exibição usando atributo: `ThumbHorizAlign` e atributo: `ThumbVertAlign`. A composição dimensionada é então mesclada com o modo de exibição preenchido sem dimensionamento adicional. Quaisquer áreas do composto que se estendem além do retângulo de exibição são cortadas.
