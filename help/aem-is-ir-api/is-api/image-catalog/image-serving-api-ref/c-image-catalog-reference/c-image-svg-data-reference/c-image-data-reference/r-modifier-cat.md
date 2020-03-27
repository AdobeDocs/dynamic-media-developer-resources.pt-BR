---
description: Sequência do modificador da solicitação de prefixo. Nenhum ou mais comandos do Servidor de imagens separados por '&' caracteres.
seo-description: Sequência do modificador da solicitação de prefixo. Nenhum ou mais comandos do Servidor de imagens separados por '&' caracteres.
seo-title: Modificador
solution: Experience Manager
title: Modificador
topic: Scene7 Image Serving - Image Rendering API
uuid: eb17d115-22ec-4b1b-9039-9bd2bc256f48
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Modificador{#modifier}

Sequência do modificador da solicitação de prefixo. Nenhum ou mais comandos do Servidor de imagens separados por &#39;&amp;&#39; caracteres.

Usado para modificar imagens e armazenar o corpo dos modelos de forma persistente.

Os comandos nesse campo são substituídos pelos mesmos comandos na solicitação ou modelo a partir do qual esse registro é referenciado e pelos comandos em `catalog::PostModifier`

As macros são permitidas no, desde `catalog::Modifier`que estejam definidas no mesmo catálogo ou no catálogo padrão. As variáveis personalizadas também podem ser usadas.

## Propriedades {#section-6674388f77d644469371a17e8809c45f}

Sequência de caracteres de texto. Opcional.

## Padrão {#section-f4ffe8b75792435c8b1040e75c5fb8a1}

Nenhum.

## Consulte também {#section-7a67803d141b442180c418c1f3cff029}

[catálogo::PostModifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md#reference-4bc3738a812b4e7c8a180e27bfbd770b)
