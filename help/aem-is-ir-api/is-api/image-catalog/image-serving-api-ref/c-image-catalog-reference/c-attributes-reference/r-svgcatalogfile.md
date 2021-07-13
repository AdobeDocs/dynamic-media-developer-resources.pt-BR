---
description: Caminhos do arquivo de dados SVG. Especifica os arquivos que contêm os dados SVG para este catálogo.
solution: Experience Manager
title: SvgCatalogFile
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 654579a2-33ff-4633-a6d0-3c03ec8d5aed
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---

# SvgCatalogFile{#svgcatalogfile}

Caminhos do arquivo de dados SVG. Especifica os arquivos que contêm os dados SVG para este catálogo.

Os arquivos de dados SVG são carregados após todos os arquivos de dados de imagem, na ordem exata especificada. Se o mesmo valor `catalog::Id` ocorrer em mais de um registro (na mesma imagem ou em arquivos de catálogo SVG diferentes), a última instância prevalecerá.

## Propriedades {#section-fc2d549f76474792837b2b92ec2087ea}

Um ou mais valores de string de texto, separados por vírgulas. Opcional. Cada valor deve ser um caminho ou caminho de arquivo absoluto relativo à pasta de catálogo.

## Padrão {#section-a4e58951f3c249599665b823566433c9}

Vazio, o que indica que este catálogo de imagens não inclui dados SVG.

## Consulte também {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[Dados](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29) do catálogo,  [CatalogFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
