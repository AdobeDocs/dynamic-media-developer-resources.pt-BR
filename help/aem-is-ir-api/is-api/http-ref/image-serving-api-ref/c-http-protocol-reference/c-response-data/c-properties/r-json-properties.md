---
title: Propriedades JSONP
description: Se jsonp for especificado como o formato de resposta, os dados de resposta serão formatados usando JSONP (JavaScript Object Notation with Padding), encapsulado em uma chamada de função JavaScript.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
source-git-commit: d1df6e943747f9db12c08003647aee840fdfcc0a
workflow-type: tm+mt
source-wordcount: '206'
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

A variável `s7jsonResponse` A função JavaScript deve ser definida pelo cliente. Em sua forma mais simples, a função pode ter esta aparência:

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

As solicitações que oferecem suporte ao formato de resposta JSONP permitem especificar o nome do manipulador de retorno de chamada JS usando a sintaxe estendida de `req=` parâmetro:

`req=...,json [&handler = reqHandler]`

A variável `<reqHandler>` sintaxe é o nome do manipulador JS presente na resposta JSONP. Somente caracteres a-z, A-Z e 0-9 são permitidos. Opcional. O padrão é `s7jsonResponse`.

O pacote Visualizadores do Servidor de imagens da Dynamic Media inclui um utilitário para solicitar e analisar dados formatados em JSONP do Servidor de imagens.

Consulte [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) para obter mais informações sobre o formato JSONP.

Consulte [www.json.org](https://www.json.org/json-en.html) para obter mais informações sobre o formato JSON.

Consulte também [solic](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
