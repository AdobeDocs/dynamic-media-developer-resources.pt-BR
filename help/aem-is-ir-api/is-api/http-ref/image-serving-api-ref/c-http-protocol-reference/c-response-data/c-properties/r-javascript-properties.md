---
description: Se JavaScript™ for especificado como o formato de resposta, os dados de resposta serão formatados para serem analisados como um arquivo de inclusão JavaScript™.
solution: Experience Manager
title: Propriedades do JavaScript™
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 12e69221-4a2c-4ec6-b38b-0a8d98d3c4a6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---

# Propriedades do JavaScript™{#javascript-properties}

Se JavaScript™ for especificado como o formato de resposta, os dados de resposta serão formatados para serem analisados como um arquivo de inclusão JavaScript™.

Uma resposta típica de propriedades do JavaScript™ tem esta estrutura geral:

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* pode estar em branco. O espaço em branco é opcional no início e no final de cada linha e antes e depois do separador =. Todos os valores estão entre aspas simples. Aspas simples em cadeias de caracteres são evitadas com duas aspas simples consecutivas.

Para analisar uma resposta de propriedades do JavaScript™, qualquer objeto ou objeto referenciado na resposta deve ser criado antes que o arquivo de propriedades seja carregado. Veja a seguir um exemplo de como usar `req=props` para obter o tamanho da imagem de resposta no JavaScript™:

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```
