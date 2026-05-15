---
description: Esteja ciente destas regras de miniatura.
solution: Experience Manager
title: Regras de miniatura
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
TQID: 'https://experienceleague.adobe.com/2HjWzEcMFnTFzwDWz-Ld7wZ6FsFcq3gwaUFcSWgxPko'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 0%

---

# Regras de miniatura{#thumbnail-rules}

Esteja ciente destas regras de miniatura.

1. Se `catalog::ThumbType=Crop`, a imagem (cortada) será dimensionada para o menor tamanho possível, enquanto ainda cobrirá todo o retângulo de destino. Se `catalog::ThumbType=Fit`, a imagem (cortada) será dimensionada para o maior tamanho possível e ainda será ajustada para a imagem inteira no retângulo de destino. Se `catalog::ThumbType=Texture`, a imagem (cortada) é dimensionada para a proporção de `catalog::ThumbRes` para `catalog::Resolution`.
1. Alinhe a imagem dimensionada com o retângulo de destino com base em `attribute::ThumbHorizAlign` e `attribute::ThumbVertAlign`.
1. Cortar o resultado para o retângulo de destino.
