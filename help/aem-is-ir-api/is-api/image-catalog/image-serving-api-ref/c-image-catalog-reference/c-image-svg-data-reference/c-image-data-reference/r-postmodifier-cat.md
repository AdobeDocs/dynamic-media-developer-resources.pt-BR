---
description: Sequência do modificador da solicitação de sufixo. Nenhum ou mais comandos do Image Serving separados por caracteres '&'.
solution: Experience Manager
title: PostModifier
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---


# PostModifier{#postmodifier}

Sequência do modificador da solicitação de sufixo. Nenhum ou mais comandos do Image Serving separados por caracteres &#39;&amp;&#39;.

Os comandos neste campo sempre substituem comandos na solicitação HTTP e em `catalog::Modifier`.

`catalog::PostModifier` é útil se determinadas imagens exigirem configurações especiais que são normalmente controladas pelo URL, como  `qlt=` ou  `resmode=`. `catalog::Modifier` deve ser usada para definir a maioria dos comandos IS no catálogo de imagens.

As macros são permitidas em `catalog::PostModifier`, desde que sejam definidas no mesmo catálogo ou no catálogo padrão. Variáveis personalizadas também podem ser usadas.

>[!NOTE]
>
>Se uma solicitação envolver várias camadas, somente o conteúdo de `catalog::PostModifier` da camada 0 será aplicado. `catalog::PostModifier` de todas as outras camadas é ignorada.

## Propriedades {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

Sequência de texto. Opcional.

## Padrão {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

Nenhum.

## Consulte também {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[catálogo:Modificador](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
