---
description: Se o xml for especificado como o formato de resposta, os dados de resposta serão formatados como um documento XML que pode ser analisado por qualquer analisador XML padrão.
seo-description: Se o xml for especificado como o formato de resposta, os dados de resposta serão formatados como um documento XML que pode ser analisado por qualquer analisador XML padrão.
seo-title: Propriedades XML
solution: Experience Manager
title: Propriedades XML
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9d169ad2-e466-4ab3-8900-ea9c6125edad
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# Propriedades XML{#xml-properties}

Se o xml for especificado como o formato de resposta, os dados de resposta serão formatados como um documento XML que pode ser analisado por qualquer analisador XML padrão.

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

O elemento `<prop-group>` é usado como o container mais externo e para agrupar propriedades. Se um grupo for nomeado, o nome corresponderá ao nome do objeto Java/JavaScript.

>[!NOTE]
>
>A codificação de caracteres pode ser especificada para alguns tipos `req=`. Consulte a descrição do comando específico `req=`para obter detalhes.

