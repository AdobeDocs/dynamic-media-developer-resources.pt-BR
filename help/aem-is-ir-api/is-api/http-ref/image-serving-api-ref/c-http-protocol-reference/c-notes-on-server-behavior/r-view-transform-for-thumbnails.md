---
description: A imagem retornada ao cliente em resposta a uma solicitação req=tmb é derivada da imagem composta considerando os seguintes valores wid=, hei=, atributo DefaultThumbPix e atributo MaxPix.
solution: Experience Manager
title: Exibir transformação de miniaturas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
TQID: 'https://experienceleague.adobe.com/yx1jgWnx-cwMDmBY2NOzYEyEjCqehPqGBK31MvGo-4o'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 245
ht-degree: 0%

---

# Exibir transformação de miniaturas{#view-transform-for-thumbnails}

A imagem retornada ao cliente em resposta a uma solicitação req=tmb é derivada da imagem composta considerando os seguintes valores: wid=, hei=, attribute::DefaultThumbPix e attribute::MaxPix.

1. **Calcular o retângulo de exibição** - Use `wid=` ou o valor de largura de `attribute::DefaultThumbPix` para a largura do retângulo de exibição. Use `hei=` ou o valor de altura de `attribute::DefaultThumbPix` para a altura. O direito de exibição deve ser totalmente especificado nesta etapa. (Observe que o retângulo de exibição é o mesmo que o retângulo da camada 0, se nenhum `size=` for especificado para a camada 0).
1. **Dimensionar o composto** - Se `catalog::ThumbType=Crop`, o composto será dimensionado para a menor imagem possível enquanto ainda estiver preenchendo a exibição inteira; os dados de imagem extras serão cortados. Se `catalog::ThumbType= Fit`, então o composto é dimensionado para a maior imagem possível enquanto ainda se ajusta todo o composto para a vista correta. Se `catalog::ThumbType=Texture`, a composição não será dimensionada para preservar a resolução especificada em `catalog::ThumbRes`.
1. **Preencher e cortar** - O retângulo de exibição é preenchido com a `bgc=` cor (ou, se não especificado, com `attribute::ThumbBkgColor`). O composto escalonado está alinhado com a exibição rect usando atributo:: `ThumbHorizAlign` e atributo:: `ThumbVertAlign`. O composto escalonado é então mesclado com a visualização preenchida rect sem dimensionamento adicional. Qualquer área do composto que se estenda além do retângulo de exibição é cortada.
