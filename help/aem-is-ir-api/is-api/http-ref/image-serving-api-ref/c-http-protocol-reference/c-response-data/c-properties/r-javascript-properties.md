---
description: Se o javascript for especificado como o formato de resposta, os dados de resposta serão formatados para serem analisados como um arquivo de inclusão JavaScript.
seo-description: Se o javascript for especificado como o formato de resposta, os dados de resposta serão formatados para serem analisados como um arquivo de inclusão JavaScript.
seo-title: Propriedades do JavaScript
solution: Experience Manager
title: Propriedades do JavaScript
topic: Scene7 Image Serving - Image Rendering API
uuid: 832a927e-ecaf-438c-8fbf-a702d58902d8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Propriedades do JavaScript{#javascript-properties}

Se o javascript for especificado como o formato de resposta, os dados de resposta serão formatados para serem analisados como um arquivo de inclusão JavaScript.

Uma resposta de propriedades típica do JavaScript tem esta estrutura geral:

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* pode estar vazio. O espaço em branco é opcional no início e no final de cada linha e antes e depois do separador =. Todos os valores são delimitados por aspas simples. Aspas simples em strings são escapadas com duas aspas simples consecutivas.

Para analisar uma resposta de propriedades JavaScript, qualquer objeto referenciado na resposta deve ser criado antes que o arquivo de propriedades seja carregado. Veja a seguir um exemplo para usar `req=props` para obter o tamanho da imagem de resposta no JavaScript:

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```

