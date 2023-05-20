---
description: Dados do mapa de imagem.
solution: Experience Manager
title: mapa
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '208'
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

Devoluções `catalog::Map` sem modificação ao consultar uma entrada de catálogo simples sem comandos adicionais especificados (não dimensionará para `catalog::maxPix`).

Se qualquer outro comando for especificado na solicitação, um mapa de imagem composta será retornado, derivado por dimensionamento, recorte, rotação e disposição em camadas de todos `catalog::Map` e/ou `map=` comandos incluídos na solicitação, da mesma forma que os dados de imagem seriam com `req=img`.

Especificar `text` ou omita o segundo parâmetro para retornar os dados do mapa de imagem na forma de um `HTML <AREA>` string do elemento com tipo de resposta MIME `text/plain`.

Especificar `xml` para formatar a resposta como XML em vez de HTML. A codificação de texto pode ser especificada opcionalmente. O padrão é `UTF-8`.

Retorna uma cadeia de caracteres vazia (ou vazia) `<AREA>` elemento) se nenhum dado de mapa for encontrado para os objetos de catálogo especificados, e/ou se nenhum `<AREA>` Os elementos do permanecem após o recorte das imagens.

A resposta HTTP pode ser armazenada em cache com o TTL com base em `catalog::Expiration`.

As solicitações que oferecem suporte ao formato de resposta JSONP permitem especificar o nome do manipulador de retorno de chamada JS usando a sintaxe estendida de `req=` parâmetro:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` é o nome do manipulador JS presente na resposta JSONP. Somente caracteres a-z, A-Z e 0-9 são permitidos. Opcional. O padrão é `s7jsonResponse`.

Consulte [Mapas de imagem](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
