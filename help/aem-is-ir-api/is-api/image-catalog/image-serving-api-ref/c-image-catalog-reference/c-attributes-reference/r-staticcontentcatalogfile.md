---
description: Caminhos de arquivos de dados do catálogo de conteúdo estático. Especifica os arquivos que contêm os dados de conteúdo estático para este catálogo.
solution: Experience Manager
title: ArquivoCatálogoDeConteúdoEstático
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ff6f0ad8-189f-4172-89cb-f138d2df8fe4
TQID: 'https://experienceleague.adobe.com/98uNzMz83z3lfa2d3LNixYKZzUWWE9zqrK1fnPo-JNA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 116
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
