---
description: Esteja ciente dessas regras de miniatura.
solution: Experience Manager
title: Regras de miniatura
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# Regras de miniatura{#thumbnail-rules}

Esteja ciente dessas regras de miniatura.

1. Se `catalog::ThumbType=Crop`, a imagem (cortada) será dimensionada para o menor tamanho possível enquanto ainda cobre todo o destino direto. Se `catalog::ThumbType=Fit`, a imagem (cortada) será dimensionada para o maior tamanho possível, ao mesmo tempo em que ainda ajusta a imagem inteira ao retângulo de destino. Se `catalog::ThumbType=Texture`, a imagem (cortada) é dimensionada para a proporção de `catalog::ThumbRes` para `catalog::Resolution`.
1. Alinhe a imagem dimensionada com o redirecionamento de destino com base em `attribute::ThumbHorizAlign` e `attribute::ThumbVertAlign`.
1. Recorte o resultado no gráfico de destino.
