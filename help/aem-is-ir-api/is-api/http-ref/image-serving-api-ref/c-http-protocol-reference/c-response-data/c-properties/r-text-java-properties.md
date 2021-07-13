---
description: Se o texto for especificado como o formato de resposta, os dados de resposta serão formatados para serem legíveis como propriedades Java.
solution: Experience Manager
title: Propriedades de texto (Java)
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# Propriedades de texto (Java){#text-java-properties}

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

*`propertyValue`* pode estar em branco. O espaço em branco é opcional no início e no fim de cada linha e antes e depois do separador =. Aspas simples ou duplas podem ser usadas para delimitar valores de string, mas não são obrigatórias.

Os valores de string podem conter caracteres de escape no estilo JAVA, como `\n`, `\t`, `\:` ou `\\`.
