---
description: Dados do mapa de imagens.
seo-description: Dados do mapa de imagens.
seo-title: mapa
solution: Experience Manager
title: mapa
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 57cb0fcf-5a07-4109-bfd4-ef9aaf794b27
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---


# map{#map}

Dados do mapa de imagens.

`req=map[,text|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> codificação</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Identificador de solicitação exclusivo. </p></td> 
 </tr> 
</table>

Retorna `catalog::Map` sem modificação ao consultar uma entrada de catálogo simples sem comandos adicionais especificados (não será dimensionado para `catalog::maxPix`).

Se qualquer outro comando for especificado na solicitação, um mapa de imagem composta será retornado, o que é derivado do dimensionamento, recorte, giro e disposição em camadas de todos os comandos `catalog::Map` e/ou `map=` incluídos na solicitação, da mesma forma que os dados de imagem seriam com `req=img`.

Especifique `text` ou omita o segundo parâmetro para retornar os dados do mapa de imagem em forma de uma string de elemento `HTML <AREA>` com tipo MIME de resposta `text/plain`.

Especifique `xml` para formatar a resposta como XML em vez de HTML. A codificação de texto pode ser especificada opcionalmente. O padrão é `UTF-8`.

Retorna uma string vazia (ou elemento `<AREA>` vazio) se nenhum dado de mapa foi encontrado para os objetos de catálogo especificados e/ou se nenhum elemento `<AREA>` permanecer após o corte das imagens.

A resposta HTTP pode ser armazenada em cache com o TTL baseado em `catalog::Expiration`.

As solicitações compatíveis com o formato de resposta JSONP permitem que você especifique o nome do manipulador de retorno de chamada JS usando a sintaxe estendida do parâmetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` é o nome do manipulador JS presente na resposta JSONP. Somente caracteres a-z, A-Z e 0-9 são permitidos. Opcional. O padrão é `s7jsonResponse`.

Consulte [Mapas de imagem](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
