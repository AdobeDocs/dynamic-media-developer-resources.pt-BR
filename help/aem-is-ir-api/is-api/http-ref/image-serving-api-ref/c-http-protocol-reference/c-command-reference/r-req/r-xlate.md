---
description: Versões específicas à localidade disponíveis. Retorna uma lista de versões específicas à localidade disponíveis da ID do catálogo especificada no caminho da solicitação.
seo-description: Versões específicas à localidade disponíveis. Retorna uma lista de versões específicas à localidade disponíveis da ID do catálogo especificada no caminho da solicitação.
seo-title: xlate
solution: Experience Manager
title: xlate
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 4c2370e5-1d46-4242-89bb-a5ce416ef63c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 2%

---


# xlate{#xlate}

Versões específicas à localidade disponíveis. Retorna uma lista de versões específicas à localidade disponíveis da ID do catálogo especificada no caminho da solicitação.

`req=xlate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8970A3A5A64F4DC2B184E251993390C5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Identificador de solicitação exclusivo. </p></td> 
 </tr> 
</table>

Consulte [Tradução da Id do Objeto](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414).

Por exemplo:

`xlate.translatedIds=image,image_fr,image_de`

A resposta HTTP pode ser armazenada em cache com o TTL baseado em `catalog::Expiration`.

As solicitações compatíveis com o formato de resposta JSONP permitem que você especifique o nome do manipulador de retorno de chamada JS usando a sintaxe estendida do parâmetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` é o nome do manipulador JS presente na resposta JSONP. Somente caracteres a-z, A-Z e 0-9 são permitidos. Opcional. O padrão é `s7jsonResponse`.
