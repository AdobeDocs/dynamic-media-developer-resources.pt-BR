---
description: Sufixo do arquivo de imagem padrão. Anexado ao valor do campo Caminho do catálogo (ou MaskPath do catálogo) se o caminho não incluir um sufixo de arquivo
solution: Experience Manager
title: DefaultExt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 43b3e5b8-6374-458d-8503-8e04c8c84233
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---

# DefaultExt{#defaultext}

Sufixo do arquivo de imagem padrão. Anexado ao valor do campo catalog::Path (ou catalog::MaskPath) se o caminho não incluir um sufixo de arquivo

Um sufixo de arquivo consiste em um ponto e um ou mais caracteres entre o ponto e o final da string. O sufixo será anexado ao caminho http se o caminho não for resolvido para uma entrada de catálogo e se o último elemento do caminho não incluir um sufixo de arquivo.

## Propriedades {#section-b024e6450b414ccc8b83a48a3b4e00f9}

String de texto. Deve incluir um &#39;.&#39; à esquerda e um ou mais caracteres.

## Padrão {#section-1194c36ffe0748c5b9ff7d732a506588}

Herdado de `default::DefaultExt` se não estiver definido. Se definido, mas vazio, nenhum sufixo padrão é aplicado aos nomes de imagem ao usar esse catálogo.

## Consulte também {#section-d7c408b979844643adff8258f500eb7c}

[catálogo::Caminho](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
