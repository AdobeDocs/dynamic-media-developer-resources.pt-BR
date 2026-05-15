---
title: Propriedades JSONP
description: Se jsonp for especificado como o formato de resposta, os dados de resposta serão formatados usando JSONP (JavaScript Object Notation with Padding), encapsulado em uma chamada de função JavaScript.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
TQID: 'https://experienceleague.adobe.com/pMirwhZ5n0mVuK2If4kJz3XDQZPDhORJCZBLsDf2C8I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 212
ht-degree: 0%

---

# Propriedades JSONP{#jsonp-properties}

Se jsonp for especificado como o formato de resposta, os dados de resposta serão formatados usando JSONP (JavaScript Object Notation with Padding), encapsulado em uma chamada de função JavaScript.

O cliente pode especificar um identificador de solicitação exclusivo opcional ( *`reqId`*), que é retornado na resposta e permite que o cliente diferencie várias respostas recebidas de forma assíncrona. Uma resposta típica tem a seguinte estrutura geral:

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

A função JavaScript `s7jsonResponse` deve ser definida pelo cliente. Em sua forma mais simples, a função pode ter esta aparência:

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

As solicitações que oferecem suporte ao formato de resposta JSONP permitem especificar o nome do manipulador de retorno de chamada JS usando a sintaxe estendida do parâmetro `req=`:

`req=...,json [&handler = reqHandler]`

A sintaxe `<reqHandler>` é o nome do manipulador JS presente na resposta JSONP. Somente caracteres a-z, A-Z e 0-9 são permitidos. Opcional. O padrão é `s7jsonResponse`.

O pacote de visualizadores do Dynamic Media Image Serving inclui um utilitário para solicitar e analisar dados formatados em JSONP do Image Serving.

Consulte [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) para obter mais informações sobre o formato JSONP.

Consulte [www.json.org](https://www.json.org/json-en.html) para obter mais informações sobre o formato JSON.

Consulte também [req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
