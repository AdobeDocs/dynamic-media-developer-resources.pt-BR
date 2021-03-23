---
description: Âncora da imagem. Ponto de origem quando essa imagem é usada como uma camada em um modelo ou imagem composta.
seo-description: Âncora da imagem. Ponto de origem quando essa imagem é usada como uma camada em um modelo ou imagem composta.
seo-title: Âncora
solution: Experience Manager
title: Âncora
uuid: 81069578-8470-4ec0-b755-47b0a8124024
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# Âncora{#anchor}

Âncora da imagem. Ponto de origem quando essa imagem é usada como uma camada em um modelo ou imagem composta.

Também define o ponto central padrão para rotação.

## Propriedades {#section-95740f14160744e7bc763094b8be40d8}

Dois números inteiros, separados por vírgula. Deslocamento de pixels em relação ao canto superior esquerdo da imagem de resolução completa.

Substituído por `anchor=` (que, por sua vez, pode ser substituído por `origin=`).

## Padrão {#section-ca3a4cc837d643519eff15951f2b47a1}

O ponto central da imagem é usado se esse campo não estiver presente ou se estiver vazio e se for um registro de imagem válido (ou seja, se `catalog::Path` for válido).

## Consulte também {#section-f605d29c3f5d48ad8e2a374f11886f19}

[âncora=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) ,  [origem=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
