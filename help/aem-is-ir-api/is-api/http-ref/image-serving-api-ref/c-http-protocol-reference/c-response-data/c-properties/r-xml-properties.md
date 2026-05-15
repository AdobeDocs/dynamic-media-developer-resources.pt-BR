---
description: Se xml for especificado como o formato de resposta, os dados de resposta serão formatados como um documento XML que pode ser analisado por qualquer analisador XML padrão.
solution: Experience Manager
title: Propriedades XML
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84cae0cd-d13b-409e-bd65-71c7e973d4b8
TQID: 'https://experienceleague.adobe.com/Nljy83DDIbeY6l-d6F02NlaFzyCFJny7iesxnF9mFyo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 109
ht-degree: 0%

---

# Propriedades XML{#xml-properties}

Se xml for especificado como o formato de resposta, os dados de resposta serão formatados como um documento XML que pode ser analisado por qualquer analisador XML padrão.

Um documento de resposta de propriedades típicas tem esta estrutura geral:

```
<?xml version="1.0" encoding="UTF-8" ?>
<prop-group>
   <prop-group name="
<varname>
  objectName
</varname>">
       <property name="
<varname>
  propertyName
</varname>" value="
<varname>
  propertyValue
</varname>" />
       ...
    </prop-group>
 ...
</prop-group>
```

O elemento `<prop-group>` é usado como o contêiner mais externo e para agrupar propriedades. Se um grupo for nomeado, o nome corresponderá ao nome do objeto Java/JavaScript.

>[!NOTE]
>
>A codificação de caracteres pode ser especificada para alguns `req=` tipos. Consulte a descrição do comando `req=` específico para obter detalhes.
