---
description: Os dados de propriedade consistem em uma string de texto que representa uma ou mais propriedades.
seo-description: Os dados de propriedade consistem em uma string de texto que representa uma ou mais propriedades.
seo-title: Dados de propriedade
solution: Experience Manager
title: Dados de propriedade
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7fa6ae70-8d70-41d6-9e47-7df3d616874c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# Dados de propriedade{#property-data}

Os dados de propriedade consistem em uma string de texto que representa uma ou mais propriedades.

Uma propriedade consiste em um nome de propriedade e um valor de propriedade, separados por =.

Várias propriedades são separadas por separadores de linha, que podem ser `??` ou `<CR><LF>`. Se toda a cadeia de dados da propriedade não estiver entre aspas, o servidor substituirá cada ocorrência de `??` por `<CR><LF>` antes de transmitir os dados ao cliente. Os nomes de propriedades podem consistir em letras, números, &#39;.&#39;, &#39;-&#39; e &#39;_&#39;. Os nomes de propriedades não fazem distinção entre maiúsculas e minúsculas.

Os valores de propriedade não devem incluir separadores de linha.

Consulte [Cadeia de caracteres de texto](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) para obter regras adicionais aplicadas aos dados de propriedade.
