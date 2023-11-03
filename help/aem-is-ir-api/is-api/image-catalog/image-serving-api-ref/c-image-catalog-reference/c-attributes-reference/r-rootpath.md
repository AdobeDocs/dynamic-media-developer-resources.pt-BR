---
description: Caminho raiz dos dados de origem. Caminho absoluto ou relativo da pasta raiz para os dados de origem deste catálogo de imagens.
solution: Experience Manager
title: RootPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 06662b27-fb10-41d0-a14c-48025d7e9137
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---

# RootPath{#rootpath}

Caminho raiz dos dados de origem. Caminho absoluto ou relativo da pasta raiz para os dados de origem deste catálogo de imagens.

A variável `RootPath` é um valor de string de texto. Consulte [Gerenciamento de dados de origem](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e) para obter informações adicionais sobre os caminhos de raiz do servidor.

## Propriedades {#section-b41d7e0ea63143eb8034569706cad0c0}

String de texto. Deve ser um caminho de pasta relativo ou um caminho absoluto válido acessível pelo Servidor de imagens.

## Padrão {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

Herdado de `default::RootPath` se não estiver definido. Se definido, mas vazio, não contribui para o caminho raiz do arquivo de origem.

## Consulte também {#section-6bf4ffc4987843a9a2dbe81b43076437}

[catálogo::Caminho](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md),  [conjunto de regras::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [Gerenciamento de dados de origem](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)
