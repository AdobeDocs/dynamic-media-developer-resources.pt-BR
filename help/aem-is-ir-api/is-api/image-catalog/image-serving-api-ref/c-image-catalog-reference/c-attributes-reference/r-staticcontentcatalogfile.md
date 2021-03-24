---
description: Caminhos do arquivo de dados do catálogo de conteúdo estático. Especifica os arquivos que contêm os dados de conteúdo estático para este catálogo.
solution: Experience Manager
title: StaticContentCatalogFile
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# StaticContentCatalogFile{#staticcontentcatalogfile}

Caminhos do arquivo de dados do catálogo de conteúdo estático. Especifica os arquivos que contêm os dados de conteúdo estático para este catálogo.

Os arquivos de dados do catálogo de conteúdo estático são carregados na ordem especificada. Se o mesmo valor `static::Id` ocorrer em mais de um registro (no mesmo ou em arquivos de catálogo diferentes), a última instância prevalecerá.

## Propriedades {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

Um ou mais valores de string de texto, separados por vírgulas. Opcional. Cada valor deve ser um caminho ou caminho de arquivo absoluto relativo à pasta de catálogo.

## Padrão {#section-702edfbc00c54fc29e412a3ff99fef2b}

Vazio, o que indica que este catálogo de imagens não inclui dados de conteúdo estático.

## Consulte também {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[Dados do catálogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
