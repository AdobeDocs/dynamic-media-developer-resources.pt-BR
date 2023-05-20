---
description: A imagem retornada ao cliente em resposta a uma solicitação req=tmb é derivada da imagem composta considerando os seguintes valores wid=, hei=, atributo DefaultThumbPix e atributo MaxPix.
solution: Experience Manager
title: Exibir transformação de miniaturas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# Exibir transformação de miniaturas{#view-transform-for-thumbnails}

A imagem retornada ao cliente em resposta a uma solicitação req=tmb é derivada da imagem composta considerando os seguintes valores: wid=, hei=, attribute::DefaultThumbPix e attribute::MaxPix.

1. **Calcular a visualização correta** - Utilização `wid=` ou o valor da largura de `attribute::DefaultThumbPix` para a largura do retângulo de exibição. Uso `hei=` ou o valor da altura de `attribute::DefaultThumbPix` para a altura. O direito de exibição deve ser totalmente especificado nesta etapa. (Observe que o retângulo de exibição é o mesmo que o retângulo da camada 0, se não `size=`é especificado para a camada 0).
1. **Dimensionar o composto** - Se `catalog::ThumbType=Crop`, o composto é dimensionado para a menor imagem possível enquanto ainda preenche todo o retângulo de exibição; os dados de imagem extras são cortados. Se `catalog::ThumbType= Fit`, então o composto é dimensionado para a maior imagem possível, enquanto ainda ajusta todo o composto na reta de exibição. Se `catalog::ThumbType=Texture`, o composto não é dimensionado para preservar a resolução especificada em `catalog::ThumbRes`.
1. **Preenchimento e corte** - O direito de visualização é preenchido com o `bgc=` cor (ou, se não especificado, com `attribute::ThumbBkgColor`). O composto escalonado é alinhado com a visualização rect usando o atributo:: `ThumbHorizAlign` atributo e: `ThumbVertAlign`. O composto escalonado é então mesclado com a visualização preenchida rect sem dimensionamento adicional. Qualquer área do composto que se estenda além do retângulo de exibição é cortada.
