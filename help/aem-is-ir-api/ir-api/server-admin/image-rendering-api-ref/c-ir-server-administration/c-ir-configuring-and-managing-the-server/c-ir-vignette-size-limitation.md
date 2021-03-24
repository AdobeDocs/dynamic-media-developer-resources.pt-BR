---
description: A Renderização de imagem impõe uma limitação de tamanho de dois Megapixels para vinhetas não-pirâmides.
solution: Experience Manager
title: Limitação do tamanho da vinheta
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---


# Limitação do tamanho da vinheta{#vignette-size-limitation}

A Renderização de imagem impõe uma limitação de tamanho de dois Megapixels para vinhetas não-pirâmides.

Modifique o valor de `IrMaxNonPyrVignetteSize` em [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] se o aplicativo exigir suporte para vinhetas não-pirâmides com uma área de imagem (largura x altura) maior que esse limite.

>[!NOTE]
>
>`attribute::MaxPix` e também  `IS::MaxMessageSize` pode precisar ser ajustado para permitir tamanhos de imagem de resposta invulgarmente grandes. Consulte a documentação do Image Serving para obter detalhes.

