---
description: Sufixo padrão do arquivo de imagem. Anexado ao valor de campo Caminho do catálogo (ou Caminho da máscara do catálogo) se o caminho não incluir um sufixo de arquivo
solution: Experience Manager
title: DefaultExt
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# DefaultExt{#defaultext}

Sufixo padrão do arquivo de imagem. Anexado ao valor do campo catalog::Path (ou catalog::MaskPath) se o caminho não incluir um sufixo de arquivo

Um sufixo de arquivo consiste em um ponto e um ou mais caracteres entre o ponto e o fim da string. O sufixo é anexado ao caminho http, se o caminho não for resolvido para uma entrada de catálogo e se o último elemento de caminho não incluir um sufixo de arquivo.

## Propriedades {#section-b024e6450b414ccc8b83a48a3b4e00f9}

Sequência de texto. Deve incluir um &#39;.&#39; à esquerda. e um ou mais caracteres.

## Padrão {#section-1194c36ffe0748c5b9ff7d732a506588}

Herdado de `default::DefaultExt` se não estiver definido. Se definido, mas vazio, nenhum sufixo padrão é aplicado aos nomes das imagens ao usar este catálogo.

## Consulte também {#section-d7c408b979844643adff8258f500eb7c}

[catálogo::Caminho](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [catálogo::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
