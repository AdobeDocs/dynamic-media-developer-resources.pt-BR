---
description: A imagem retornada ao cliente em resposta a uma solicitação req=tmb é derivada da imagem composta considerando os seguintes valores wid=, hei=, atributo DefaultThumbPix e atributo MaxPix.
solution: Experience Manager
title: Exibir transformação para miniaturas
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---


# Exibir transformação para miniaturas{#view-transform-for-thumbnails}

A imagem retornada ao cliente em resposta a uma solicitação req=tmb é derivada da imagem composta considerando os seguintes valores: wid=, hei=, atributo::DefaultThumbPix e atributo::MaxPix.

1. **Calcule o sinal de exibição**  - Use  `wid=` ou o valor de largura de  `attribute::DefaultThumbPix` para a largura do sinal de exibição. Use `hei=` ou o valor da altura `attribute::DefaultThumbPix` para a altura. O direito de exibição deve ser totalmente especificado nesta etapa. (Observe que o reto de exibição será o mesmo que o reto da camada 0, se nenhum `size=`for especificado para a camada 0).
1. **Dimensionar o compósito**  - Se  `catalog::ThumbType=Crop`, o compósito será dimensionado para a menor imagem possível enquanto ainda preencherá todo o retângulo de exibição; os dados de imagem extras são cortados. Se `catalog::ThumbType= Fit`, o compósito será dimensionado para a maior imagem possível, ao mesmo tempo que ainda ajusta todo o compósito para o retângulo de exibição. Se `catalog::ThumbType=Texture`, o composto não é dimensionado de forma alguma para preservar a resolução especificada em `catalog::ThumbRes`.
1. **Preencher e cortar**  - O gráfico de exibição é preenchido com a  `bgc=` cor (ou, se não especificado, com  `attribute::ThumbBkgColor`). O composto dimensionado é alinhado com o direito de exibição usando atributo: `ThumbHorizAlign` e atributo: `ThumbVertAlign`. A composição dimensionada é então mesclada com o modo de exibição preenchido sem dimensionamento adicional. Quaisquer áreas do composto que se estendem além do retângulo de exibição são cortadas.

