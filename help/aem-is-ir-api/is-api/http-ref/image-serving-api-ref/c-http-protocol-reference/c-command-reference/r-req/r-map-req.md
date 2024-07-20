---
title: mapa
description: Dados do mapa de imagem.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# mapa{#map}

Dados do mapa de imagem.

`req=map[,text|{xml[, *`codificação`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> codificação</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Identificador exclusivo da solicitação. </p></td> 
 </tr> 
</table>

Retorna `catalog::Map` sem modificação ao consultar uma entrada de catálogo simples sem comandos adicionais especificados (não dimensiona para `catalog::maxPix`).

Se qualquer outro comando for especificado na solicitação, um mapa de imagem composta será retornado. O mapa de imagem composta é derivado do dimensionamento, recorte, rotação e disposição em camadas de todos os comandos `catalog::Map` e/ou `map=` incluídos na solicitação, da mesma forma que os dados de imagem seriam com `req=img`.

Especifique `text` ou omita o segundo parâmetro para que você possa retornar os dados do mapa de imagem na forma de uma cadeia de caracteres de elemento `HTML <AREA>` com tipo MIME de resposta `text/plain`.

Especifique `xml` para poder formatar a resposta como XML em vez de HTML. A codificação de texto pode ser especificada opcionalmente. O padrão é `UTF-8`.

Retorna uma cadeia de caracteres vazia (ou elemento `<AREA>` vazio) se nenhum dado de mapa for encontrado para os objetos de catálogo especificados e/ou se nenhum elemento `<AREA>` permanecer após o corte das imagens.

A resposta HTTP pode ser armazenada em cache com o TTL com base em `catalog::Expiration`.

As solicitações que oferecem suporte ao formato de resposta JSONP permitem especificar o nome do manipulador de retorno de chamada JS usando a sintaxe estendida do parâmetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` é o nome do manipulador JS presente na resposta JSONP. Somente caracteres a-z, A-Z e 0-9 são permitidos. Opcional. O padrão é `s7jsonResponse`.

Consulte [Mapas de imagens](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
