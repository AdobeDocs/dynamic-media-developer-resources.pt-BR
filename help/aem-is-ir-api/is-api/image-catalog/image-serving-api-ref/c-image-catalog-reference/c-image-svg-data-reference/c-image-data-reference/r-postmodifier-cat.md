---
description: Sequência do modificador da solicitação de sufixo. Nenhum ou mais comandos do Servidor de imagens separados por '&' caracteres.
seo-description: Sequência do modificador da solicitação de sufixo. Nenhum ou mais comandos do Servidor de imagens separados por '&' caracteres.
seo-title: PostModifier
solution: Experience Manager
title: PostModifier
topic: Scene7 Image Serving - Image Rendering API
uuid: 8800a9b2-e9c0-498b-b4e1-37952ba7c842
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PostModifier{#postmodifier}

Sequência do modificador da solicitação de sufixo. Nenhum ou mais comandos do Servidor de imagens separados por &#39;&amp;&#39; caracteres.

Os comandos nesse campo sempre substituem os comandos na solicitação HTTP e no `catalog::Modifier`.

`catalog::PostModifier` é útil se determinadas imagens exigem configurações especiais que são normalmente controladas pelo URL, como `qlt=` ou `resmode=`. `catalog::Modifier` deve ser usado para definir a maioria dos comandos IS no catálogo de imagens.

As macros são permitidas no, desde `catalog::PostModifier`que estejam definidas no mesmo catálogo ou no catálogo padrão. As variáveis personalizadas também podem ser usadas.

>[!NOTE]
>
>Se uma solicitação envolver várias camadas, somente o conteúdo `catalog::PostModifier` da camada 0 será aplicado. `catalog::PostModifier` de todas as outras camadas é ignorada.

## Propriedades {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

Sequência de caracteres de texto. Opcional.

## Padrão {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

Nenhum.

## Consulte também {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[catálogo:Modificador](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
