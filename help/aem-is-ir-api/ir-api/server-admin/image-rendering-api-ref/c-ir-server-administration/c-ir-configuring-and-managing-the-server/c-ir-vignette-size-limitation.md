---
description: A Renderização de imagem impõe uma limitação de tamanho de dois megapixels para vinhetas que não sejam de pirâmide.
solution: Experience Manager
title: Limitação do tamanho da vinheta
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---

# Limitação do tamanho da vinheta{#vignette-size-limitation}

A Renderização de imagem impõe uma limitação de tamanho de dois megapixels para vinhetas que não sejam de pirâmide.

Modifique o valor de `IrMaxNonPyrVignetteSize` no [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] se o aplicativo exigir suporte para vinhetas que não sejam de pirâmide com uma área de imagem (largura x altura) maior que esse limite.

>[!NOTE]
>
>`attribute::MaxPix` e `IS::MaxMessageSize` A também pode precisar ser ajustada para permitir tamanhos de imagem de resposta excepcionalmente grandes. Consulte a documentação do Servidor de imagens para obter mais detalhes.
