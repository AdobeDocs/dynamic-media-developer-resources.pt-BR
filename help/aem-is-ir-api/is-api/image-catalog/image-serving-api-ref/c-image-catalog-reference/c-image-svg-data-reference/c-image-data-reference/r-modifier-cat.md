---
description: Sequência do modificador da solicitação de prefixo. Nenhum ou mais comandos do Image Serving separados por caracteres '&'.
solution: Experience Manager
title: Modificador
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---


# Modificador{#modifier}

Sequência do modificador da solicitação de prefixo. Nenhum ou mais comandos do Image Serving separados por caracteres &#39;&amp;&#39;.

Usado para modificar imagens de forma persistente e armazenar o corpo dos modelos.

Os comandos neste campo são substituídos pelos mesmos comandos na solicitação ou no modelo a partir do qual este registro é referenciado e pelos comandos em `catalog::PostModifier`

As macros são permitidas em `catalog::Modifier`, desde que sejam definidas no mesmo catálogo ou no catálogo padrão. Variáveis personalizadas também podem ser usadas.

## Propriedades {#section-6674388f77d644469371a17e8809c45f}

Sequência de texto. Opcional.

## Padrão {#section-f4ffe8b75792435c8b1040e75c5fb8a1}

Nenhum.

## Consulte também {#section-7a67803d141b442180c418c1f3cff029}

[catálogo::PostModifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md#reference-4bc3738a812b4e7c8a180e27bfbd770b)
