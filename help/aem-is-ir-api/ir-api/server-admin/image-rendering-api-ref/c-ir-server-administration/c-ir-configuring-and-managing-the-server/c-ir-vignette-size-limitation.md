---
description: A Renderização de imagem impõe uma limitação de tamanho de dois Megapixels para vinhetas não pirâmides.
seo-description: A Renderização de imagem impõe uma limitação de tamanho de dois Megapixels para vinhetas não pirâmides.
seo-title: Limitação do tamanho da vinheta
solution: Experience Manager
title: Limitação do tamanho da vinheta
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 218e8c7e-f313-47cb-af42-30c585d4ec12
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---


# Limitação do tamanho da vinheta{#vignette-size-limitation}

A Renderização de imagem impõe uma limitação de tamanho de dois Megapixels para vinhetas não pirâmides.

Modifique o valor de `IrMaxNonPyrVignetteSize` em [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] se o aplicativo exigir suporte para vinhetas não pirâmides com uma área de imagem (largura x altura) maior que esse limite.

>[!NOTE]
>
>`attribute::MaxPix` e também  `IS::MaxMessageSize` pode ser necessário ajustar para permitir tamanhos de imagem de resposta invulgarmente grandes. Consulte a documentação do Servidor de imagens para obter detalhes.

