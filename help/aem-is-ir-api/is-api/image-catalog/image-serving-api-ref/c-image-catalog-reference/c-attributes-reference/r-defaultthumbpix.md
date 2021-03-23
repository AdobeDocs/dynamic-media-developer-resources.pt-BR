---
description: Tamanho padrão da miniatura. Usado em vez do atributo DefaultPix para solicitações de miniatura (req=tmb).
seo-description: Tamanho padrão da miniatura. Usado em vez do atributo DefaultPix para solicitações de miniatura (req=tmb).
seo-title: DefaultThumbPix
solution: Experience Manager
title: DefaultThumbPix
uuid: 7b310aab-6d38-45f3-a3e7-b074a8e7a795
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---


# DefaultThumbPix{#defaultthumbpix}

Tamanho padrão da miniatura. Usado em vez do atributo::DefaultPix para solicitações de miniatura (req=tmb).

O servidor restringe as imagens de resposta a não serem maiores que essa largura e altura, se uma solicitação de miniatura ( `req=tmb`) não especificar o tamanho explicitamente não especificar o tamanho da exibição usando `wid=`, `hei=` ou `scl=`.

## Propriedades {#section-650d9b1194fb4c47a03c6809e6b4af0e}

Dois números inteiros, 0 ou maiores, separados por vírgula. Largura e altura em pixels. Qualquer um dos valores pode ser definido como 0 para mantê-los livres.

Não se aplica a solicitações aninhadas/incorporadas.

## Padrão {#section-2c4a4f14540449638822913513170ff1}

Herdado de `default::DefaultThumbPix` se não estiver definido ou se estiver vazio.

## Consulte também {#section-4ad00963ffa049fcb17ad63e6bbe7ac4}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [atributo::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
