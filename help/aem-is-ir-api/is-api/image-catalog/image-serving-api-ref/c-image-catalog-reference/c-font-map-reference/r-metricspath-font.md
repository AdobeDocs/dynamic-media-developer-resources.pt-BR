---
description: Caminho do arquivo de métricas de fonte. Caminho e nome de um arquivo de métricas de fonte, incluindo o sufixo do arquivo.
solution: Experience Manager
title: MetricsPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0f1f98a5-b53b-4e20-b4c8-e70482b01a04
TQID: 'https://experienceleague.adobe.com/XPXcnrT94IfPupctNoxqN7-qYCuxdeoqXQeBkM1Un4k'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 107
ht-degree: 0%

---

# MetricsPath{#metricspath}

Caminho do arquivo de métricas de fonte. Caminho e nome de um arquivo de métricas de fonte, incluindo o sufixo do arquivo.

Usado para fontes do Adobe Type 1. Se não for especificado, o servidor tentará localizar um arquivo de métricas de fonte na mesma pasta em que o arquivo de fonte principal está localizado. Ocorre um erro se um arquivo de métricas de fonte necessário não for encontrado no momento da renderização.

## Propriedades {#section-955268c581574875b05253d9e14544f3}

String de texto. Opcional para arquivos Adobe Type 1. Deve ser um caminho de arquivo vazio ou válido do Servidor de imagens, seja absoluto ou relativo a `attribute::RootPath`.

## Padrão {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

Nenhum.

## Consulte também {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
