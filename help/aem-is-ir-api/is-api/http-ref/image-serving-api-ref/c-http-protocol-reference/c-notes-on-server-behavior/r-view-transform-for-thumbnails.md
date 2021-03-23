---
description: A imagem retornada ao cliente em resposta a uma solicitação req=tmb é derivada da imagem composta considerando os seguintes valores wid=, hei=, atributo DefaultThumbPix e atributo MaxPix.
seo-description: A imagem retornada ao cliente em resposta a uma solicitação req=tmb é derivada da imagem composta considerando os seguintes valores wid=, hei=, atributo DefaultThumbPix e atributo MaxPix.
seo-title: Exibir transformação para miniaturas
solution: Experience Manager
title: Exibir transformação para miniaturas
uuid: 29924bc1-ada1-420f-aef7-bf9a7db7065b
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---


# Exibir transformação para miniaturas{#view-transform-for-thumbnails}

A imagem retornada ao cliente em resposta a uma solicitação req=tmb é derivada da imagem composta considerando os seguintes valores: wid=, hei=, atributo::DefaultThumbPix e atributo::MaxPix.

1. **Calcule o sinal de exibição**  - Use  `wid=` ou o valor de largura de  `attribute::DefaultThumbPix` para a largura do sinal de exibição. Use `hei=` ou o valor da altura `attribute::DefaultThumbPix` para a altura. O direito de exibição deve ser totalmente especificado nesta etapa. (Observe que o reto de exibição será o mesmo que o reto da camada 0, se nenhum `size=`for especificado para a camada 0).
1. **Dimensionar o compósito**  - Se  `catalog::ThumbType=Crop`, o compósito será dimensionado para a menor imagem possível enquanto ainda preencherá todo o retângulo de exibição; os dados de imagem extras são cortados. Se `catalog::ThumbType= Fit`, o compósito será dimensionado para a maior imagem possível, ao mesmo tempo que ainda ajusta todo o compósito para o retângulo de exibição. Se `catalog::ThumbType=Texture`, o composto não é dimensionado de forma alguma para preservar a resolução especificada em `catalog::ThumbRes`.
1. **Preencher e cortar**  - O gráfico de exibição é preenchido com a  `bgc=` cor (ou, se não especificado, com  `attribute::ThumbBkgColor`). O composto dimensionado é alinhado com o direito de exibição usando atributo: `ThumbHorizAlign` e atributo: `ThumbVertAlign`. A composição dimensionada é então mesclada com o modo de exibição preenchido sem dimensionamento adicional. Quaisquer áreas do composto que se estendem além do retângulo de exibição são cortadas.

