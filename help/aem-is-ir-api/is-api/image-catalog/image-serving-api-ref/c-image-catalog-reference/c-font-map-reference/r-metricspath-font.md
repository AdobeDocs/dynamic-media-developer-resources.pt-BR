---
description: Caminho do arquivo das métricas de fonte. Caminho e nome de um arquivo de métricas de fonte, incluindo o sufixo do arquivo.
seo-description: Caminho do arquivo das métricas de fonte. Caminho e nome de um arquivo de métricas de fonte, incluindo o sufixo do arquivo.
seo-title: MetricsPath
solution: Experience Manager
title: MetricsPath
uuid: b59110bf-330f-4ca4-8b0a-219a61d383f7
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '131'
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
