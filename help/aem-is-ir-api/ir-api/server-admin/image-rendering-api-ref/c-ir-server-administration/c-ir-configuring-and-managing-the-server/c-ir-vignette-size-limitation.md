---
description: A Renderização de imagem impõe uma limitação de tamanho de dois Megapixels para vinhetas não-pirâmides.
solution: Experience Manager
title: Limitação do tamanho da vinheta
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---

# Limitação do tamanho da vinheta{#vignette-size-limitation}

A Renderização de imagem impõe uma limitação de tamanho de dois Megapixels para vinhetas não-pirâmides.

Modifique o valor de `IrMaxNonPyrVignetteSize` em [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] se o aplicativo exigir suporte para vinhetas não-pirâmides com uma área de imagem (largura x altura) maior que esse limite.

>[!NOTE]
>
>`attribute::MaxPix` e também  `IS::MaxMessageSize` pode precisar ser ajustado para permitir tamanhos de imagem de resposta invulgarmente grandes. Consulte a documentação do Image Serving para obter detalhes.
