---
description: Se o javascript for especificado como o formato de resposta, os dados de resposta serão formatados para serem analisados como um arquivo de inclusão do JavaScript.
seo-description: Se o javascript for especificado como o formato de resposta, os dados de resposta serão formatados para serem analisados como um arquivo de inclusão do JavaScript.
seo-title: Propriedades do JavaScript
solution: Experience Manager
title: Propriedades do JavaScript
uuid: 832a927e-ecaf-438c-8fbf-a702d58902d8
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---


# Propriedades do JavaScript{#javascript-properties}

Se o javascript for especificado como o formato de resposta, os dados de resposta serão formatados para serem analisados como um arquivo de inclusão do JavaScript.

Uma resposta típica das propriedades do JavaScript tem essa estrutura geral:

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* pode estar em branco. O espaço em branco é opcional no início e no fim de cada linha e antes e depois do separador =. Todos os valores são entre aspas simples. Aspas simples em strings são evitadas com duas aspas simples consecutivas.

Para analisar uma resposta de propriedades do JavaScript, qualquer objeto referenciado na resposta deve ser criado antes que o arquivo de propriedades seja carregado. A seguir, um exemplo de uso de `req=props` para obter o tamanho da imagem de resposta em JavaScript:

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```

