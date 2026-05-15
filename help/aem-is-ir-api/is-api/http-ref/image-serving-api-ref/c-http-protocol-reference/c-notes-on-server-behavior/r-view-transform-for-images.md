---
description: Exibir transformação para imagens
solution: Experience Manager
title: Exibir transformação para imagens
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
TQID: 'https://experienceleague.adobe.com/PPSeNhcaJ4Nx8ojXOt9vqJFp7F9NGo4LO3UxdLKzmwo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 271
ht-degree: 0%

---

# Exibir transformação para imagens{#view-transform-for-images}

A imagem retornada ao cliente em resposta a uma solicitação `req=img` é derivada da imagem composta considerando os seguintes valores: `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix` e o tamanho da imagem composta.

Se `wid=` e `hei=` forem especificados, e `scl=` não for, a imagem composta será dimensionada de forma que se ajuste totalmente à exibição correta definida por `wid=` e `hei=`. Se a proporção da view rect for diferente da imagem composta, a imagem composta dimensionada será alinhada dentro da view rect usando o valor `align=`, se especificado, ou será centralizada de outra forma. Qualquer espaço não coberto pelos dados de imagem é preenchido com `bgc=` ou, se não especificado, com `attribute::BkgColor`.

Se `scl=` for especificado, a imagem composta será dimensionada de acordo com esse fator de escala. Se `wid=` e/ou `hei=` também for especificado, a imagem dimensionada será cortada para `wid=` e/ou `hei=` ou um espaço extra será adicionado, conforme necessário. `align=` especifica onde a imagem é cortada ou o espaço extra é adicionado, e qualquer espaço extra é preenchido com `bgc=` ou `attribute::BkgColor`.

Se `wid=`, `hei=` ou `scl=` não forem especificados e se a largura ou a altura da imagem composta exceder `attribute::DefaultPix`, a imagem composta será dimensionada para não exceder `attribute::DefaultPix`. Caso contrário, a imagem composta será usada sem dimensionamento.

Para garantir que a imagem de exibição seja retornada sem qualquer outro dimensionamento, especifique `scl=1`.

Se `rgn=` for especificado, a imagem de resposta será cortada adequadamente para chegar ao tamanho final da imagem de resposta. Esse tamanho é comparado com `attribute::MaxPix` (se definido), e um erro será gerado se a imagem de resposta for maior em qualquer uma das dimensões.

Se `fmt=` especificar dados sem alfa, quaisquer áreas transparentes na imagem de resposta serão preenchidas com `bgc=` ou `attribute::BkgColor`.
