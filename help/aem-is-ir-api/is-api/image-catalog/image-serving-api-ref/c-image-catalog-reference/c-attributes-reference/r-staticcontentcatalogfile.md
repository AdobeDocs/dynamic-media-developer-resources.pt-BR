---
description: Caminhos do arquivo de dados do catálogo de conteúdo estático. Especifica os arquivos que contêm os dados de conteúdo estático para este catálogo.
seo-description: Caminhos do arquivo de dados do catálogo de conteúdo estático. Especifica os arquivos que contêm os dados de conteúdo estático para este catálogo.
seo-title: StaticContentCatalogFile
solution: Experience Manager
title: StaticContentCatalogFile
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 82d2a68a-255a-4e65-a29f-7022e7f0f5ec
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---


# StaticContentCatalogFile{#staticcontentcatalogfile}

Caminhos do arquivo de dados do catálogo de conteúdo estático. Especifica os arquivos que contêm os dados de conteúdo estático para este catálogo.

Os arquivos de dados do catálogo de conteúdo estático são carregados na ordem especificada. Se o mesmo valor `static::Id` ocorrer em mais de um registro (no mesmo arquivo de catálogo ou em arquivos de catálogo diferentes), a última instância prevalecerá.

## Propriedades {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

Um ou mais valores de string de texto, separados por vírgulas. Opcional. Cada valor deve ser um caminho ou caminho de arquivo absoluto relativo à pasta do catálogo.

## Padrão {#section-702edfbc00c54fc29e412a3ff99fef2b}

Vazio, que indica que este catálogo de imagens não inclui nenhum dado de conteúdo estático.

## Consulte também {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[Dados do catálogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
