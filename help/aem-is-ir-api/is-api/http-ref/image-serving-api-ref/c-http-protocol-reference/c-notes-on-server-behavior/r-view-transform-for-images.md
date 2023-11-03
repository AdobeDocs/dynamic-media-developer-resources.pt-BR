---
description: Exibir transformação para imagens
solution: Experience Manager
title: Exibir transformação para imagens
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Exibir transformação para imagens{#view-transform-for-images}

A imagem retornada ao cliente em resposta a um erro `req=img` é derivada da imagem composta considerando os seguintes valores: `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix`e o tamanho da imagem composta.

Se `wid=` e `hei=` são especificados e `scl=` não for, a imagem composta será dimensionada de modo que se ajuste totalmente à função view definida por `wid=` e `hei=`. Se a proporção da imagem de exibição reta for diferente da imagem composta, a imagem composta dimensionada será alinhada dentro da imagem reta usando a `align=` valor, se especificado, ou centralizado caso contrário. Qualquer espaço não coberto pelos dados da imagem é preenchido com `bgc=` ou, se não especificado, com `attribute::BkgColor`.

Se `scl=` for especificada, a imagem composta será dimensionada de acordo com esse fator de escala. Se `wid=` e/ou `hei=` também é especificada, a imagem dimensionada é então cortada para `wid=` e/ou `hei=` ou espaço extra, conforme necessário. `align=` especifica onde a imagem é cortada ou o espaço extra é adicionado e qualquer espaço extra é preenchido com `bgc=` ou `attribute::BkgColor`.

Se nenhuma delas `wid=`, `hei=` nem `scl=` são especificados e se a largura ou a altura da imagem composta exceder `attribute::DefaultPix`, a imagem composta será dimensionada para não exceder `attribute::DefaultPix`. Caso contrário, a imagem composta será usada sem dimensionamento.

Para garantir que a imagem de exibição seja retornada sem qualquer outro dimensionamento, especifique `scl=1`.

Se `rgn=` for especificada, a imagem de resposta será cortada de acordo para chegar ao tamanho final da imagem de resposta. Esse tamanho é comparado com `attribute::MaxPix` (se definido), e um erro será gerado se a imagem de resposta for maior em qualquer dimensão.

Se `fmt=` especifica dados sem alfa, quaisquer áreas transparentes na imagem de resposta são preenchidas com `bgc=` ou `attribute::BkgColor`.
