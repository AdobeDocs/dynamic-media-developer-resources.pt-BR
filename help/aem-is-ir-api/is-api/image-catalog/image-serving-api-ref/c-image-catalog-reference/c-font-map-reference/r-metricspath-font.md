---
description: Caminho do arquivo de métricas de fonte. Caminho e nome de um arquivo de métricas de fonte, incluindo o sufixo do arquivo.
seo-description: Caminho do arquivo de métricas de fonte. Caminho e nome de um arquivo de métricas de fonte, incluindo o sufixo do arquivo.
seo-title: MetricsPath
solution: Experience Manager
title: MetricsPath
topic: Scene7 Image Serving - Image Rendering API
uuid: b59110bf-330f-4ca4-8b0a-219a61d383f7
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# MetricsPath{#metricspath}

Caminho do arquivo de métricas de fonte. Caminho e nome de um arquivo de métricas de fonte, incluindo o sufixo do arquivo.

Usada para fontes do Tipo 1 de Adobe. Se não for especificado, o servidor tentará localizar um arquivo de métricas de fonte na mesma pasta em que o arquivo de fonte principal está localizado. Um erro ocorrerá se um arquivo de métricas de fonte necessário não puder ser encontrado no momento da renderização.

## Propriedades {#section-955268c581574875b05253d9e14544f3}

Sequência de caracteres de texto. Opcional para arquivos do Tipo 1 de Adobe. Deve estar vazio ou ser um caminho de arquivo do Servidor de imagens válido, seja absoluto ou relativo a `attribute::RootPath`.

## Padrão {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

Nenhum.

## Consulte também {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[atributo::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
