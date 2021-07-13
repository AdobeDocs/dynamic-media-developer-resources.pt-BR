---
description: Caminho do arquivo das métricas de fonte. Caminho e nome de um arquivo de métricas de fonte, incluindo o sufixo do arquivo.
solution: Experience Manager
title: MetricsPath
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 0f1f98a5-b53b-4e20-b4c8-e70482b01a04
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# MetricsPath{#metricspath}

Caminho do arquivo das métricas de fonte. Caminho e nome de um arquivo de métricas de fonte, incluindo o sufixo do arquivo.

Usado para fontes Adobe Type 1. Se não for especificado, o servidor tentará localizar um arquivo de métricas de fonte na mesma pasta em que o arquivo de fonte principal está localizado. Um erro ocorrerá se um arquivo de métricas de fonte necessário não for encontrado no momento da renderização.

## Propriedades {#section-955268c581574875b05253d9e14544f3}

Sequência de texto. Opcional para arquivos Adobe Type 1. Deve estar vazio ou ser um caminho de arquivo do Servidor de Imagens válido, absoluto ou relativo a `attribute::RootPath`.

## Padrão {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

Nenhum.

## Consulte também {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[atributo::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
