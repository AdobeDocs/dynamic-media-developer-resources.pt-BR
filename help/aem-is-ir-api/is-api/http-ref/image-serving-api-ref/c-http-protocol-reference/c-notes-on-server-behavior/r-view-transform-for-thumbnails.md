---
description: A imagem devolvida ao cliente em resposta a uma solicitação req=tmb é derivada da imagem composta considerando os seguintes valores wid=, hei=, atributo DefaultThumbPix e atributo MaxPix.
seo-description: A imagem devolvida ao cliente em resposta a uma solicitação req=tmb é derivada da imagem composta considerando os seguintes valores wid=, hei=, atributo DefaultThumbPix e atributo MaxPix.
seo-title: Transformação de visualização para miniaturas
solution: Experience Manager
title: Transformação de visualização para miniaturas
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 29924bc1-ada1-420f-aef7-bf9a7db7065b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# Transformação de visualização para miniaturas{#view-transform-for-thumbnails}

A imagem retornada ao cliente em resposta a uma solicitação req=tmb é derivada da imagem composta considerando os seguintes valores: wid=, hei=, atributo::DefaultThumbPix e atributo::MaxPix.

1. **Calcule o retângulo**  de visualização - Use  `wid=` ou o valor de largura  `attribute::DefaultThumbPix` para a largura do retângulo de visualização. Use `hei=` ou o valor de altura de `attribute::DefaultThumbPix` para a altura. A visualização rect deve ser totalmente especificada nesta etapa. (Observe que o retângulo de visualização será igual ao retângulo de camada 0, se nenhum `size=`for especificado para a camada 0).
1. **Dimensionar o composto**  - Se  `catalog::ThumbType=Crop`, o composto é dimensionado para a menor imagem possível enquanto ainda preenche todo o retângulo de visualização; os dados de imagem extra são cortados. Se `catalog::ThumbType= Fit`, o composto será dimensionado para a maior imagem possível, ainda que encaixe o composto inteiro no retângulo da visualização. Se `catalog::ThumbType=Texture`, o composto não é dimensionado para preservar a resolução especificada em `catalog::ThumbRes`.
1. **Preencher e recortar**  - o retângulo de visualização é preenchido com a  `bgc=` cor (ou, se não for especificado, com  `attribute::ThumbBkgColor`). A composição dimensionada é alinhada com o retângulo de visualização usando o atributo: `ThumbHorizAlign` e atributo: `ThumbVertAlign`. O composto dimensionado é então mesclado com o retângulo de visualização preenchido sem mais dimensionamento. Todas as áreas do composto que se estendem além do retângulo da visualização são cortadas.

