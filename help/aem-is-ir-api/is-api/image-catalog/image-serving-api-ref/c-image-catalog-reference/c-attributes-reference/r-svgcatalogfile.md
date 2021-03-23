---
description: Caminhos do arquivo de dados SVG. Especifica os arquivos que contêm os dados SVG para este catálogo.
seo-description: Caminhos do arquivo de dados SVG. Especifica os arquivos que contêm os dados SVG para este catálogo.
seo-title: SvgCatalogFile
solution: Experience Manager
title: SvgCatalogFile
uuid: f0c8e687-77cc-4ca7-b2c2-6ba8960e11e6
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '138'
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
