---
description: Se jsonp for especificado como o formato de resposta, os dados de resposta serão formatados usando JSONP (JavaScript Object Nation with Padding), encapsulado em uma chamada de função JavaScript.
solution: Experience Manager
title: Propriedades JSONP
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# Propriedades JSONP{#jsonp-properties}

Se jsonp for especificado como o formato de resposta, os dados de resposta serão formatados usando JSONP (JavaScript Object Nation with Padding), encapsulado em uma chamada de função JavaScript.

O cliente pode especificar um identificador de solicitação único opcional ( *`reqId`*), que é retornado na resposta e permite que o cliente diferencie várias respostas recebidas de forma assíncrona. Uma resposta típica tem a seguinte estrutura geral:

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

A função JavaScript `s7jsonResponse` deve ser definida pelo cliente. Na forma mais simples, a função pode ter esta aparência:

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

As solicitações que oferecem suporte ao formato de resposta JSONP permitem especificar o nome do manipulador de retorno de chamada JS usando a sintaxe estendida do parâmetro `req=`:

`req=...,json [&handler = reqHandler]`

`<reqHandler>` é o nome do manipulador JS presente na resposta JSONP. Somente caracteres a-z, A-Z e 0-9 são permitidos. Opcional. O padrão é `s7jsonResponse`.

O pacote Dynamic Media Image Serving Viewers inclui um utilitário para solicitar e analisar dados formatados em JSONP do Image Serving.

Consulte [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) para obter mais informações sobre o formato JSONP.

Consulte [www.json.org](https://www.json.org) para obter mais informações sobre o formato JSON.

Consulte também [req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
