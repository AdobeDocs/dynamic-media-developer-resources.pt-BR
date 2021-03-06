---
description: Os dados de propriedade consistem em uma string de texto que representa uma ou mais propriedades.
solution: Experience Manager
title: Dados de propriedade
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 86278720-ece0-4e67-8fb1-443355f878b7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# Dados de propriedade{#property-data}

Os dados de propriedade consistem em uma string de texto que representa uma ou mais propriedades.

Uma propriedade consiste em um nome de propriedade e um valor de propriedade, separados por =.

Várias propriedades são separadas por separadores de linha, que podem ser `??` ou `<CR><LF>`. Se toda a cadeia de dados da propriedade não estiver entre aspas, o servidor substituirá cada ocorrência de `??` por `<CR><LF>` antes de transmitir os dados ao cliente. Os nomes de propriedades podem consistir em letras, números, &#39;.&#39;, &#39;-&#39; e &#39;_&#39;. Os nomes de propriedades não fazem distinção entre maiúsculas e minúsculas.

Os valores de propriedade não devem incluir separadores de linha.

Consulte [Cadeia de caracteres de texto](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) para obter regras adicionais aplicadas aos Dados de propriedade.
