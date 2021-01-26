---
description: Sufixo de arquivo de imagem padrão. Anexado ao valor do campo Caminho do catálogo (ou Caminho da máscara do catálogo) se o caminho não incluir um sufixo de arquivo
seo-description: Sufixo de arquivo de imagem padrão. Anexado ao valor do campo Caminho do catálogo (ou Caminho da máscara do catálogo) se o caminho não incluir um sufixo de arquivo
seo-title: DefaultExt
solution: Experience Manager
title: DefaultExt
topic: Dynamic Media Image Serving - Image Rendering API
uuid: aa245d18-15cc-41cb-a49d-757d74fe6231
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# DefaultExt{#defaultext}

Sufixo de arquivo de imagem padrão. Anexado ao valor do campo catálogo::Path (ou catálogo::MaskPath) se o caminho não incluir um sufixo de arquivo

Um sufixo de arquivo consiste em um ponto e um ou mais caracteres entre o ponto e o final da string. O sufixo é anexado ao caminho http, se o caminho não for resolvido para uma entrada de catálogo e se o último elemento de caminho não incluir um sufixo de arquivo.

## Propriedades {#section-b024e6450b414ccc8b83a48a3b4e00f9}

Sequência de caracteres de texto. Deve incluir um &#39;.&#39; à esquerda. e um ou mais caracteres.

## Padrão {#section-1194c36ffe0748c5b9ff7d732a506588}

Herdado de `default::DefaultExt` se não estiver definido. Se definido, mas vazio, nenhum sufixo padrão é aplicado aos nomes de imagem ao usar esse catálogo.

## Consulte também {#section-d7c408b979844643adff8258f500eb7c}

[catálogo::Caminho](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [catálogo::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
