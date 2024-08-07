---
description: Caminhos de arquivos de dados do catálogo de conteúdo estático. Especifica os arquivos que contêm os dados de conteúdo estático para este catálogo.
solution: Experience Manager
title: ArquivoCatálogoDeConteúdoEstático
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ff6f0ad8-189f-4172-89cb-f138d2df8fe4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---

# ArquivoCatálogoDeConteúdoEstático{#staticcontentcatalogfile}

Caminhos de arquivos de dados do catálogo de conteúdo estático. Especifica os arquivos que contêm os dados de conteúdo estático para este catálogo.

Os arquivos de dados do catálogo de conteúdo estático são carregados na ordem especificada. Se o mesmo valor `static::Id` ocorrer em mais de um registro (no mesmo ou em arquivos de catálogo diferentes), a última instância prevalecerá.

## Propriedades {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

Um ou mais valores de cadeia de texto, separados por vírgulas. Opcional. Cada valor deve ser um caminho de arquivo absoluto ou um caminho relativo para a pasta do catálogo.

## Padrão {#section-702edfbc00c54fc29e412a3ff99fef2b}

Vazio, que indica que esse catálogo de imagens não inclui dados de conteúdo estáticos.

## Consulte também {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[Dados do catálogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
