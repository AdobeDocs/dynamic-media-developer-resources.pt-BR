---
description: Transformação de visualização para imagens
solution: Experience Manager
title: Transformação de visualização para imagens
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 8594f746-0e58-4a59-933c-a44dc0b06c25
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---


# Transformação de visualização para imagens{#view-transform-for-images}

A imagem retornada ao cliente em resposta a uma solicitação `req=img` é derivada da imagem composta considerando os seguintes valores: `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix` e o tamanho da imagem composta.

Se `wid=` e `hei=` forem especificados e `scl=` não forem, a imagem composta será dimensionada de modo que se ajuste totalmente ao retângulo de visualização definido por `wid=` e `hei=`. Se a proporção do retângulo de visualização for diferente da imagem composta, a imagem composta dimensionada será alinhada dentro do retângulo de visualização usando o valor `align=`, se especificado, ou será centralizada de outra forma. Qualquer espaço não coberto por dados de imagem é preenchido com `bgc=` ou, se não for especificado, com `attribute::BkgColor`.

Se `scl=` for especificado, a imagem composta será dimensionada pelo fator de escala. Se `wid=` e/ou `hei=` também for especificado, a imagem dimensionada será cortada em `wid=` e/ou `hei=` ou será adicionado espaço extra, conforme necessário. `align=` especifica onde a imagem é cortada ou onde um espaço extra é adicionado, e qualquer espaço extra é preenchido com  `bgc=` ou  `attribute::BkgColor`.

Se `wid=`, `hei=` ou `scl=` não forem especificados e se a largura ou a altura da imagem composta excederem `attribute::DefaultPix`, a imagem composta será dimensionada para não exceder `attribute::DefaultPix`. Caso contrário, a imagem composta será usada sem dimensionamento.

Para garantir que a imagem de visualização seja retornada sem qualquer dimensionamento adicional, especifique `scl=1`.

Se `rgn=` for especificado, a imagem de resposta será cortada adequadamente para chegar ao tamanho final da imagem de resposta. Esse tamanho é comparado com `attribute::MaxPix` (se definido), e um erro é gerado se a imagem de resposta for maior em ambas as dimensões.

Se `fmt=` especificar dados sem alfa, quaisquer áreas transparentes na imagem de resposta serão preenchidas com `bgc=` ou `attribute::BkgColor`.
