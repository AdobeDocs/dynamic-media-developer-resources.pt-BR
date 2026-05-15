---
description: Se o texto for especificado como o formato de resposta, os dados de resposta serão formatados para serem legíveis como propriedades Java.
solution: Experience Manager
title: Propriedades do texto (Java)
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
TQID: 'https://experienceleague.adobe.com/WNIuNvCPLdbeweHB5gkcFfeZu2WDDUk53us6SHtmO-A'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 0%

---

# Propriedades do texto (Java){#text-java-properties}

Se o texto for especificado como o formato de resposta, os dados de resposta serão formatados para serem legíveis como propriedades Java.

Uma resposta de propriedades de texto típica tem esta estrutura geral:

```
#S7Z OK
#
<varname>
  timeStamp
</varname>
<varname>
  objectName.propertyName
</varname>=
<varname>
  propertyValue
</varname>
...
```

*`propertyValue`* pode estar vazio. O espaço em branco é opcional no início e no final de cada linha e antes e depois do separador =. Aspas simples ou duplas podem ser usadas para delimitar valores de cadeias de caracteres, mas não são obrigatórias.

Os valores da cadeia de caracteres podem conter caracteres de escape no estilo JAVA, como `\n`, `\t`, `\:` ou `\\`.
