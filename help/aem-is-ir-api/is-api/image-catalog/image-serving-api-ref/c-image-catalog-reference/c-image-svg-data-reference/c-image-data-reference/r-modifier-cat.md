---
description: Cadeia modificadora de solicitação de prefixo. Nenhum ou mais comandos do Servidor de imagens separados por caracteres '&'.
solution: Experience Manager
title: Modificador
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6eef3159-c082-469b-b9dc-29acb28560d6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---

# Modificador{#modifier}

Cadeia modificadora de solicitação de prefixo. Nenhum ou mais comandos do Servidor de imagens separados por caracteres &#39;&amp;&#39;.

Usado para modificar persistentemente imagens e armazenar o corpo de modelos.

Os comandos neste campo são substituídos pelos mesmos comandos na solicitação ou no modelo do qual esse registro é referenciado e pelos comandos em `catalog::PostModifier`

As macros são permitidas em `catalog::Modifier`, desde que estejam definidas no mesmo catálogo ou no catálogo padrão. Variáveis personalizadas também podem ser usadas.

## Propriedades {#section-6674388f77d644469371a17e8809c45f}

String de texto. Opcional.

## Padrão {#section-f4ffe8b75792435c8b1040e75c5fb8a1}

Nenhum.

## Consulte também {#section-7a67803d141b442180c418c1f3cff029}

[catálogo::PostModifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md#reference-4bc3738a812b4e7c8a180e27bfbd770b)
