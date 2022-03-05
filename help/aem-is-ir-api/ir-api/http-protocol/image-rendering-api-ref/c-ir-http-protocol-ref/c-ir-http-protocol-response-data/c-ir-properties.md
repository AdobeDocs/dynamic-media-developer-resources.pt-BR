---
title: Propriedades
description: Os dados da propriedade são retornados em resposta ao seguinte req= types imageprops e props.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a27ec5e4-7499-44ac-8db1-bf5d67f59632
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# Propriedades{#properties}

Os dados da propriedade são retornados em resposta aos seguintes tipos req= : imageprops e props.

Os dados de resposta são formatados para serem legíveis como propriedades do Java™. Uma resposta de propriedades de texto típica tem esta estrutura geral:

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` Pode estar em branco. O espaço em branco é opcional no início e no fim de cada linha e antes e depois do separador &#39;=&#39;. Aspas simples ou duplas podem ser usadas para delimitar valores de string, mas não são obrigatórias.

Os valores da string podem conter caracteres de escape no estilo JAVA, como `\n`, `\t`, `\:`ou `\\`.

**Consulte também**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
