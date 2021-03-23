---
description: A Renderização de imagem impõe uma limitação de tamanho de dois Megapixels para vinhetas não-pirâmides.
seo-description: A Renderização de imagem impõe uma limitação de tamanho de dois Megapixels para vinhetas não-pirâmides.
seo-title: Limitação do tamanho da vinheta
solution: Experience Manager
title: Limitação do tamanho da vinheta
uuid: 218e8c7e-f313-47cb-af42-30c585d4ec12
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# Limitação do tamanho da vinheta{#vignette-size-limitation}

A Renderização de imagem impõe uma limitação de tamanho de dois Megapixels para vinhetas não-pirâmides.

Modifique o valor de `IrMaxNonPyrVignetteSize` em [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] se o aplicativo exigir suporte para vinhetas não-pirâmides com uma área de imagem (largura x altura) maior que esse limite.

>[!NOTE]
>
>`attribute::MaxPix` e também  `IS::MaxMessageSize` pode precisar ser ajustado para permitir tamanhos de imagem de resposta invulgarmente grandes. Consulte a documentação do Image Serving para obter detalhes.

