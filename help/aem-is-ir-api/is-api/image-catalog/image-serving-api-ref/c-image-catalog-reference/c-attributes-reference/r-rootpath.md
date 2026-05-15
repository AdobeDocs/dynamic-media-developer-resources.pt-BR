---
description: Caminho raiz de dados do Source. Caminho absoluto ou relativo da pasta raiz para os dados de origem deste catálogo de imagens.
solution: Experience Manager
title: RootPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 06662b27-fb10-41d0-a14c-48025d7e9137
TQID: 'https://experienceleague.adobe.com/WFDqweSZS1tNJppprC8pJblN-7LBKRM-IHt2Vfj3oW0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 111
ht-degree: 0%

---

# RootPath{#rootpath}

Caminho raiz de dados do Source. Caminho absoluto ou relativo da pasta raiz para os dados de origem deste catálogo de imagens.

O `RootPath` é um valor de cadeia de texto. Consulte [Gerenciando Dados do Source](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e) para obter informações adicionais sobre os caminhos raiz do servidor.

## Propriedades {#section-b41d7e0ea63143eb8034569706cad0c0}

String de texto. Deve ser um caminho de pasta relativo ou um caminho absoluto válido acessível pelo Servidor de imagens.

## Padrão {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

Herdado de `default::RootPath` se não estiver definido. Se definido, mas vazio, não contribui para o caminho raiz do arquivo de origem.

## Consulte também {#section-6bf4ffc4987843a9a2dbe81b43076437}

[catálogo::Caminho](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [catálogo::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md), [conjunto de regras::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [Gerenciamento de Dados do Source](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)
