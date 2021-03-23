---
description: Esteja ciente dessas regras de miniatura.
seo-description: Esteja ciente dessas regras de miniatura.
seo-title: Regras de miniatura
solution: Experience Manager
title: Regras de miniatura
uuid: 7d04b923-e062-4764-9e48-99a7bba72d3f
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---


# Regras de miniatura{#thumbnail-rules}

Esteja ciente dessas regras de miniatura.

1. Se `catalog::ThumbType=Crop`, a imagem (cortada) será dimensionada para o menor tamanho possível enquanto ainda cobre todo o destino direto. Se `catalog::ThumbType=Fit`, a imagem (cortada) será dimensionada para o maior tamanho possível, ao mesmo tempo em que ainda ajusta a imagem inteira ao retângulo de destino. Se `catalog::ThumbType=Texture`, a imagem (cortada) é dimensionada para a proporção de `catalog::ThumbRes` para `catalog::Resolution`.
1. Alinhe a imagem dimensionada com o redirecionamento de destino com base em `attribute::ThumbHorizAlign` e `attribute::ThumbVertAlign`.
1. Recorte o resultado no gráfico de destino.

