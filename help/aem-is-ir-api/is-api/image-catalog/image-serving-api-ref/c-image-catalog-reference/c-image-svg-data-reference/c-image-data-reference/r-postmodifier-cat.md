---
description: Sequência do modificador de solicitação Postfix. Nenhum ou mais comandos do Servidor de imagens separados por caracteres '&'.
solution: Experience Manager
title: PostModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d6c9408-1f09-464d-8a69-eabdf7c0117d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# PostModifier{#postmodifier}

Sequência do modificador de solicitação Postfix. Nenhum ou mais comandos do Servidor de imagens separados por caracteres &#39;&amp;&#39;.

Os comandos neste campo sempre substituem os comandos na solicitação HTTP e em `catalog::Modifier`.

`catalog::PostModifier` é útil se determinadas imagens exigirem configurações especiais que normalmente são controladas da URL, como `qlt=` ou `resmode=`. `catalog::Modifier` deve ser usado para definir a maioria dos comandos IS no catálogo de imagens.

As macros são permitidas em `catalog::PostModifier`, desde que estejam definidas no mesmo catálogo ou no catálogo padrão. Variáveis personalizadas também podem ser usadas.

>[!NOTE]
>
>Se uma solicitação envolve várias camadas, somente o conteúdo de `catalog::PostModifier` da camada 0 é aplicado. `catalog::PostModifier` de todas as outras camadas é ignorado.

## Propriedades {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

String de texto. Opcional.

## Padrão {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

Nenhum.

## Consulte também {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[catálogo::Modificador](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
