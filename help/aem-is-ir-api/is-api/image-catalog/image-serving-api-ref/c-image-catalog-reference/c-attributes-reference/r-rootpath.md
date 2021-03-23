---
description: Caminho raiz dos dados de origem. Caminho absoluto ou relativo da pasta raiz para os dados de origem deste catálogo de imagens.
seo-description: Caminho raiz dos dados de origem. Caminho absoluto ou relativo da pasta raiz para os dados de origem deste catálogo de imagens.
seo-title: RootPath
solution: Experience Manager
title: RootPath
uuid: 859bebf2-5ee7-4daa-8970-a18bddcee684
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---


# RootPath{#rootpath}

Caminho raiz dos dados de origem. Caminho absoluto ou relativo da pasta raiz para os dados de origem deste catálogo de imagens.

O `RootPath` é um valor de string de texto. Consulte [Gerenciando Dados de Origem](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e) para obter informações adicionais sobre os caminhos raiz do servidor.

## Propriedades {#section-b41d7e0ea63143eb8034569706cad0c0}

Sequência de texto. Deve estar vazio, um caminho de pasta relativo válido ou um caminho absoluto válido acessível pelo Servidor de Imagens.

## Padrão {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

Herdado de `default::RootPath` se não estiver definido. Se definido, mas vazio, não contribuirá para o caminho raiz do arquivo de origem.

## Consulte também {#section-6bf4ffc4987843a9a2dbe81b43076437}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md),   [ruleset::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e),  [Managing Source Data](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)
