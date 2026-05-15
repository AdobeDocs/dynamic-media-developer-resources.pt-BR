---
description: Caminhos de arquivos de dados do SVG. Especifica os arquivos que contêm os dados SVG para este catálogo.
solution: Experience Manager
title: SvgCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 654579a2-33ff-4633-a6d0-3c03ec8d5aed
TQID: 'https://experienceleague.adobe.com/m1-nKj-KiVQlN70GYy1AFAAQN-M1wnxTGmmj-e3t9AY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 115
ht-degree: 0%

---

# SvgCatalogFile{#svgcatalogfile}

Caminhos de arquivos de dados do SVG. Especifica os arquivos que contêm os dados SVG para este catálogo.

Os arquivos de dados do SVG são carregados após todos os arquivos de dados de imagem, na ordem exata especificada. Se o mesmo valor `catalog::Id` ocorrer em mais de um registro (na mesma imagem ou em arquivos de catálogo SVG diferentes), a última instância prevalecerá.

## Propriedades {#section-fc2d549f76474792837b2b92ec2087ea}

Um ou mais valores de cadeia de texto, separados por vírgulas. Opcional. Cada valor deve ser um caminho de arquivo absoluto ou um caminho relativo para a pasta do catálogo.

## Padrão {#section-a4e58951f3c249599665b823566433c9}

Vazio, que indica que esse catálogo de imagens não inclui dados do SVG.

## Consulte também {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[Dados de Catálogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29), [ArquivoDeCatálogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
