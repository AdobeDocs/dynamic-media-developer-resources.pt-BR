---
description: A imagem existe.
seo-description: A imagem existe.
seo-title: exists
solution: Experience Manager
title: exists
topic: Scene7 Image Serving - Image Rendering API
uuid: 5490e4c7-b52a-4b2e-b002-34afaa242c08
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# exists{#exists}

A imagem existe.

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* identificador de solicitação exclusiva

Retorna uma única propriedade chamada `catalogRecord.exists`. O valor da propriedade é definido como &quot;1&quot; se a entrada do catálogo especificada existir na imagem ou no catálogo padrão, caso contrário, ele é definido como &quot;0&quot;. `req=exists` as solicitações no `/is/content` contexto indicarão a presença ou ausência de um registro especificado no catálogo de conteúdo estático.

Outros comandos na string de solicitação são ignorados. A resposta HTTP pode ser armazenada em cache com o TTL baseado em `attribute::NonImgExpiration`.

As solicitações compatíveis com o formato de resposta JSONP permitem que você especifique o nome do manipulador de retorno de chamada JS usando a sintaxe estendida do `req=` parâmetro:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` é o nome do manipulador JS presente na resposta JSONP. Somente caracteres a-z, A-Z e 0-9 são permitidos. Opcional. O padrão é `s7jsonResponse`.
