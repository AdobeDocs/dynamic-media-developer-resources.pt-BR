---
description: A imagem existe.
solution: Experience Manager
title: existe
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---


# existe{#exists}

A imagem existe.

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* identificador de solicitação exclusiva

Retorna uma única propriedade chamada `catalogRecord.exists`. O valor da propriedade é definido como &quot;1&quot; se a entrada de catálogo especificada existir na imagem ou no catálogo padrão, caso contrário, é definido como &quot;0&quot;. `req=exists` as solicitações em relação ao  `/is/content` contexto indicarão a presença ou ausência de um registro especificado no catálogo de conteúdo estático.

Outros comandos na cadeia de caracteres de solicitação são ignorados. A resposta HTTP pode ser armazenada em cache com o TTL baseado em `attribute::NonImgExpiration`.

As solicitações que oferecem suporte ao formato de resposta JSONP permitem especificar o nome do manipulador de retorno de chamada JS usando a sintaxe estendida do parâmetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` é o nome do manipulador JS presente na resposta JSONP. Somente caracteres a-z, A-Z e 0-9 são permitidos. Opcional. O padrão é `s7jsonResponse`.
