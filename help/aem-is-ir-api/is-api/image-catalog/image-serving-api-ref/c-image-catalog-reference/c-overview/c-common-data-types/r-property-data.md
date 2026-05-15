---
description: Os dados de propriedade consistem em uma cadeia de texto que representa uma ou mais propriedades.
solution: Experience Manager
title: Dados de propriedade
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86278720-ece0-4e67-8fb1-443355f878b7
TQID: 'https://experienceleague.adobe.com/jE8U1fgDsG9wdzG4O-BsPHvPOGLXDxZRMdZvL9LuYZE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 110
ht-degree: 0%

---

# Dados de propriedade{#property-data}

Os dados de propriedade consistem em uma cadeia de texto que representa uma ou mais propriedades.

Uma propriedade consiste em um nome de propriedade e um valor de propriedade, separados por =.

Várias propriedades são separadas por separadores de linha, que podem ser `??` ou `<CR><LF>`. Se toda a cadeia de caracteres de dados da propriedade não estiver entre aspas, o servidor substituirá cada ocorrência de `??` por `<CR><LF>` antes de transmitir os dados para o cliente. Os nomes de propriedades podem consistir em letras, números, &#39;.&#39;, &#39;-&#39; e &#39;_&#39;. Os nomes de propriedades não diferenciam maiúsculas de minúsculas.

Os valores de propriedade não devem incluir separadores de linha.

Consulte [Cadeia de Caracteres de Texto](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) para obter regras adicionais aplicadas aos Dados da Propriedade.
