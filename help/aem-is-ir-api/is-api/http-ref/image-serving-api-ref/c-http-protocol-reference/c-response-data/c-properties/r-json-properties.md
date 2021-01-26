---
description: Se jsonp for especificado como o formato de resposta, os dados de resposta serão formatados usando JSONP (JavaScript Object Notation with Padding), vinculados a uma chamada de função JavaScript.
seo-description: Se jsonp for especificado como o formato de resposta, os dados de resposta serão formatados usando JSONP (JavaScript Object Notation with Padding), vinculados a uma chamada de função JavaScript.
seo-title: Propriedades JSONP
solution: Experience Manager
title: Propriedades JSONP
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e53d75f2-9b43-4e8f-8191-66f69f344cdd
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---


# Propriedades JSONP{#jsonp-properties}

Se jsonp for especificado como o formato de resposta, os dados de resposta serão formatados usando JSONP (JavaScript Object Notation with Padding), vinculados a uma chamada de função JavaScript.

O cliente pode especificar um identificador de solicitação exclusivo opcional ( *`reqId`*), que é retornado na resposta e permite que o cliente distinga várias respostas recebidas de forma assíncrona. Uma resposta típica tem a seguinte estrutura geral:

```
/*jsonp*/s7jsonResponse({ 
   " 
<varname>
  objectName 
</varname>. 
<varname>
  propertyName 
</varname>" : " 
<varname>
  propertyValue 
</varname>", 
   ... 
 }, " 
<varname>
  reqId 
</varname>" );
```

A função JavaScript `s7jsonResponse` deve ser definida pelo cliente. Em sua forma mais simples, a função pode se parecer com:

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

As solicitações compatíveis com o formato de resposta JSONP permitem que você especifique o nome do manipulador de retorno de chamada JS usando a sintaxe estendida do parâmetro `req=`:

`req=...,json [&handler = reqHandler]`

`<reqHandler>` é o nome do manipulador JS presente na resposta JSONP. Somente caracteres a-z, A-Z e 0-9 são permitidos. Opcional. O padrão é `s7jsonResponse`.

O pacote Dynamic Media Image Serving Viewers inclui um utilitário para solicitar e analisar dados formatados em JSONP do Image Serving.

Consulte [http://en.wikipedia.org/wiki/JSONP](http://en.wikipedia.org/wiki/JSONP) para obter mais informações sobre o formato JSONP.

Consulte [www.json.org](http://www.json.org) para obter mais informações sobre o formato JSON.

Consulte também [req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
