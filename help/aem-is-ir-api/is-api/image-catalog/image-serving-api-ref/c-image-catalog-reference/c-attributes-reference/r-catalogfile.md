---
description: Caminhos do arquivo de dados da imagem. Especifica os arquivos que contêm os dados da imagem para este catálogo.
solution: Experience Manager
title: CatalogFile
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---


# CatalogFile{#catalogfile}

Caminhos do arquivo de dados da imagem. Especifica os arquivos que contêm os dados da imagem para este catálogo.

Os arquivos de dados de imagem são carregados na ordem especificada. Se o mesmo valor `catalog::Id` ocorrer em mais de um registro (no mesmo ou em arquivos de catálogo diferentes), a última instância prevalecerá.

## Propriedades {#section-6da55f145ecd4e31a5de52637a436983}

Um ou mais valores de string de texto, separados por vírgulas. Opcional. Cada valor deve ser um caminho ou caminho de arquivo absoluto relativo à pasta de catálogo.

## Padrão {#section-80f91cd7a6b2479ebb310319e9c74da7}

Vazio, o que indica que este catálogo de imagem não inclui dados de imagem.

## Consulte também {#section-910b67c5041d44d99a105ad43ff63a37}

[Campos de dados do catálogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
