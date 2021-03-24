---
description: Exibir transformação de imagens
solution: Experience Manager
title: Exibir transformação de imagens
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# Exibir transformação de imagens{#view-transform-for-images}

A imagem retornada ao cliente em resposta a uma solicitação `req=img` é derivada da imagem composta considerando os seguintes valores: `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix` e o tamanho da imagem composta.

Se `wid=` e `hei=` forem especificadas e `scl=` não forem, a imagem composta será dimensionada de forma que se ajuste totalmente à exibição correta definida por `wid=` e `hei=`. Se a proporção do aspecto do gráfico de exibição for diferente da imagem composta, a imagem composta dimensionada será alinhada no gráfico de exibição usando o valor `align=`, se especificado, ou será centralizada de outra forma. Qualquer espaço não coberto por dados de imagem é preenchido com `bgc=` ou, se não especificado, com `attribute::BkgColor`.

Se `scl=` for especificado, a imagem composta será dimensionada pelo fator de escala. Se `wid=` e/ou `hei=` também for especificado, a imagem dimensionada será cortada em `wid=` e/ou `hei=` ou espaço extra será adicionado, conforme necessário. `align=` especifica onde a imagem é cortada ou o espaço extra é adicionado, e qualquer espaço extra é preenchido com  `bgc=` ou  `attribute::BkgColor`.

Se `wid=`, `hei=` ou `scl=` não forem especificadas e se a largura ou altura da imagem composta exceder `attribute::DefaultPix`, a imagem composta será dimensionada para não exceder `attribute::DefaultPix`. Caso contrário, a imagem composta será usada sem escala.

Para garantir que a imagem de exibição seja retornada sem qualquer outro dimensionamento, especifique `scl=1`.

Se `rgn=` for especificado, a imagem de resposta será cortada adequadamente para chegar ao tamanho final da imagem de resposta. Esse tamanho é comparado com `attribute::MaxPix` (se definido) e um erro é gerado se a imagem de resposta for maior em qualquer dimensão.

Se `fmt=` especificar dados sem alfa, qualquer área transparente na imagem de resposta será preenchida com `bgc=` ou `attribute::BkgColor`.
