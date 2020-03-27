---
description: Esteja ciente dessas regras de miniatura.
seo-description: Esteja ciente dessas regras de miniatura.
seo-title: Regras de miniatura
solution: Experience Manager
title: Regras de miniatura
topic: Scene7 Image Serving - Image Rendering API
uuid: 7d04b923-e062-4764-9e48-99a7bba72d3f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Regras de miniatura{#thumbnail-rules}

Esteja ciente dessas regras de miniatura.

1. Se `catalog::ThumbType=Crop`, a imagem (cortada) será dimensionada para o menor tamanho possível enquanto ainda cobre o retângulo inteiro do público alvo. Se `catalog::ThumbType=Fit`, a imagem (cortada) será dimensionada para o maior tamanho possível enquanto ainda ajusta a imagem inteira ao público alvo reto. Se `catalog::ThumbType=Texture`, a imagem (cortada) será dimensionada para a proporção de `catalog::ThumbRes` para `catalog::Resolution`.
1. Alinhe a imagem dimensionada com o retângulo do público alvo com base em `attribute::ThumbHorizAlign` e `attribute::ThumbVertAlign`.
1. Recorte o resultado para o retângulo do público alvo.

