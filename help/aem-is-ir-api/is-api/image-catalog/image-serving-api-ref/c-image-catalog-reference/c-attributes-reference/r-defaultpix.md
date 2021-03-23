---
description: Tamanho de exibição padrão.
seo-description: Tamanho de exibição padrão.
seo-title: DefaultPix
solution: Experience Manager
title: DefaultPix
uuid: f5d2e4f7-f9c5-40a5-8a64-67241fcb0242
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---


# DefaultPix{#defaultpix}

Tamanho de exibição padrão.

O servidor restringe as imagens de resposta a não serem maiores que essa largura e altura, se a solicitação não especificar o tamanho da exibição explicitamente usando `wid=`, `hei=` ou `scl=`.

## Propriedades {#section-c3e658cf82c540d986b118f74f0fe1b2}

Dois números inteiros, 0 ou maiores, separados por vírgula. Largura e altura em pixels. Qualquer um dos valores pode ser definido como 0 para mantê-los livres.

Não se aplica a solicitações aninhadas/incorporadas.

## Padrão {#section-b7338b2bf5114fff83b0714a57b20639}

Herdado de `default::DefaultPix` se não estiver definido ou se estiver vazio.

## Consulte também {#section-59088cd41da940e8ac0e74e2b049c6e9}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [catalog::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
