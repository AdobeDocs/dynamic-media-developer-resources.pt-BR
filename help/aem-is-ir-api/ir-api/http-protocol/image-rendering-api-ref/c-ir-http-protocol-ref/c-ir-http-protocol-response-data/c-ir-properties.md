---
description: Os dados da propriedade são retornados em resposta ao seguinte req= types imageprops e props.
seo-description: Os dados da propriedade são retornados em resposta ao seguinte req= types imageprops e props.
seo-title: Propriedades
solution: Experience Manager
title: Propriedades
uuid: b4e1de52-db0a-43dc-aefe-26e8f5020e79
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# Propriedades{#properties}

Os dados da propriedade são retornados em resposta aos seguintes tipos req= : imageprops e props.

Os dados de resposta são formatados para serem legíveis como propriedades Java. Uma resposta de propriedades de texto típica tem esta estrutura geral:

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` pode estar em branco. O espaço em branco é opcional no início e no fim de cada linha e antes e depois do separador &#39;=&#39;. Aspas simples ou duplas podem ser usadas para delimitar valores de string, mas não são obrigatórias.

Os valores de string podem conter caracteres de escape no estilo JAVA, como `\n`, `\t`, `\:`. ou `\\`.

**Consulte também**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
