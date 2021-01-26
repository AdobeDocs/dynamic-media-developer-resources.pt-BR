---
description: Caminhos do arquivo de dados da imagem. Especifica os arquivos que contêm os dados de imagem para este catálogo.
seo-description: Caminhos do arquivo de dados da imagem. Especifica os arquivos que contêm os dados de imagem para este catálogo.
seo-title: CatalogFile
solution: Experience Manager
title: CatalogFile
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 3599c8d3-dc4b-434e-8b11-775ea6f155ee
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# CatalogFile{#catalogfile}

Caminhos do arquivo de dados da imagem. Especifica os arquivos que contêm os dados de imagem para este catálogo.

Os arquivos de dados de imagem são carregados na ordem especificada. Se o mesmo valor `catalog::Id` ocorrer em mais de um registro (no mesmo arquivo de catálogo ou em arquivos de catálogo diferentes), a última instância prevalecerá.

## Propriedades {#section-6da55f145ecd4e31a5de52637a436983}

Um ou mais valores de string de texto, separados por vírgulas. Opcional. Cada valor deve ser um caminho ou caminho de arquivo absoluto relativo à pasta do catálogo.

## Padrão {#section-80f91cd7a6b2479ebb310319e9c74da7}

Vazio, que indica que este catálogo de imagens não inclui dados de imagem.

## Consulte também {#section-910b67c5041d44d99a105ad43ff63a37}

[Campos de dados do catálogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
