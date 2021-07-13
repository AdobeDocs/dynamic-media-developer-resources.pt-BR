---
description: Se xml for especificado como o formato de resposta, os dados de resposta serão formatados como um documento XML que pode ser analisado por qualquer analisador XML padrão.
solution: Experience Manager
title: Propriedades XML
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 84cae0cd-d13b-409e-bd65-71c7e973d4b8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '114'
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
>A codificação de caracteres pode ser especificada para alguns tipos `req=`. Consulte a descrição do comando específico `req=`para obter detalhes.
