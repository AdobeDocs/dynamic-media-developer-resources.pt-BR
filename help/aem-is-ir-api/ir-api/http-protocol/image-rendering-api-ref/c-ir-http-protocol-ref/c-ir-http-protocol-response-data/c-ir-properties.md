---
description: Os dados de propriedade são retornados em resposta aos seguintes tipos de imageprops e props.
seo-description: Os dados de propriedade são retornados em resposta aos seguintes tipos de imageprops e props.
seo-title: Propriedades
solution: Experience Manager
title: Propriedades
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b4e1de52-db0a-43dc-aefe-26e8f5020e79
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---


# Propriedades{#properties}

Os dados de propriedade são retornados em resposta aos seguintes tipos req=: imageprops e props.

Os dados de resposta são formatados para serem legíveis como propriedades Java. Uma resposta de propriedades de texto típica tem esta estrutura geral:

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` pode estar vazio. O espaço em branco é opcional no início e no fim de cada linha e antes e depois do separador &#39;=&#39;. Aspas simples ou duplos podem ser usadas para incluir valores de sequência de caracteres, mas não são obrigatórias.

Os valores de cadeia de caracteres podem conter caracteres de escape estilo JAVA, como `\n`, `\t`, `\:`. ou `\\`.

**Consulte também**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
