---
description: Se o texto for especificado como o formato de resposta, os dados de resposta serão formatados para serem legíveis como propriedades Java.
seo-description: Se o texto for especificado como o formato de resposta, os dados de resposta serão formatados para serem legíveis como propriedades Java.
seo-title: Propriedades de texto (Java)
solution: Experience Manager
title: Propriedades de texto (Java)
topic: Scene7 Image Serving - Image Rendering API
uuid: 5dba4cf7-9172-4195-968e-9ef76c25e90c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
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

*`propertyValue`* pode estar vazio. O espaço em branco é opcional no início e no final de cada linha e antes e depois do separador =. Aspas simples ou duplos podem ser usadas para incluir valores de sequência de caracteres, mas não são obrigatórias.

Os valores de cadeia de caracteres podem conter caracteres de escape estilo JAVA, como `\n`, `\t`, `\:` ou `\\`.
