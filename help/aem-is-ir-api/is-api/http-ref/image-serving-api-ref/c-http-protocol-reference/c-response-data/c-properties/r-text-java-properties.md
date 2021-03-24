---
description: Se o texto for especificado como o formato de resposta, os dados de resposta serão formatados para serem legíveis como propriedades Java.
solution: Experience Manager
title: Propriedades de texto (Java)
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '107'
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
