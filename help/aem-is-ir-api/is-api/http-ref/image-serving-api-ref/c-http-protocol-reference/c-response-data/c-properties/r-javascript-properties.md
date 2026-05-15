---
title: Propriedades do JavaScript
description: Se o JavaScript for especificado como o formato de resposta, os dados de resposta serão formatados para serem analisados como um arquivo de inclusão do JavaScript&trade;.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 12e69221-4a2c-4ec6-b38b-0a8d98d3c4a6
TQID: 'https://experienceleague.adobe.com/T6xqUHtT9XX4b9bP-wi-b0dDBe2LHE3vcBcJI6cMKqE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 137
ht-degree: 0%

---

# Propriedades do JavaScript{#javascript-properties}

Se o JavaScript for especificado como o formato de resposta, os dados de resposta serão formatados para serem analisados como um arquivo de inclusão do JavaScript.

Uma resposta típica de propriedades do JavaScript tem esta estrutura geral:

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

O *`propertyValue`* pode estar vazio. O espaço em branco é opcional no início e no final de cada linha e antes e depois do separador =. Todos os valores estão entre aspas simples. Aspas simples em cadeias de caracteres são evitadas com duas aspas simples consecutivas.

Para analisar uma resposta de propriedades do JavaScript, qualquer objeto ou objeto referenciado na resposta deve ser criado antes que o arquivo de propriedades seja carregado. Veja a seguir um exemplo de uso de `req=props` para obter o tamanho da imagem de resposta no JavaScript:

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```
