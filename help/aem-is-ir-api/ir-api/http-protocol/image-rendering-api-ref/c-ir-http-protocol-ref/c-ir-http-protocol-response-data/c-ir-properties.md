---
title: Propriedades
description: Os dados da propriedade são retornados em resposta aos seguintes tipos req= imageprops e props.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a27ec5e4-7499-44ac-8db1-bf5d67f59632
TQID: 'https://experienceleague.adobe.com/AIeKRT2-o9Z35SjXjrGECIWHFLRrdJz5JO-CkCOLj8U'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 0%

---

# Propriedades{#properties}

Os dados de propriedade são retornados em resposta aos seguintes tipos req=: imageprops e props.

Os dados de resposta são formatados para serem legíveis como propriedades Java™. Uma resposta de propriedades de texto típica tem esta estrutura geral:

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` Pode estar vazio. O espaço em branco é opcional no início e no final de cada linha e antes e depois do separador &#39;=&#39;. Aspas simples ou duplas podem ser usadas para delimitar valores de cadeias de caracteres, mas não são obrigatórias.

Os valores da cadeia de caracteres podem conter caracteres de escape no estilo JAVA, como `\n`, `\t`, `\:` ou `\\`.

**Consulte também**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)

