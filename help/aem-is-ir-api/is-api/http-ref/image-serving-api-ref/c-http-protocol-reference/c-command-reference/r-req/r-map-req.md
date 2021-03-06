---
description: Dados do mapa de imagem.
solution: Experience Manager
title: mapa
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---

# mapa{#map}

Dados do mapa de imagem.

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

Se quaisquer outros comandos forem especificados na solicitação, um mapa de imagem composta será retornado, o que é derivado por dimensionamento, recorte, rotação e camadas de todos os comandos `catalog::Map` e/ou `map=` incluídos na solicitação, da mesma forma que os dados da imagem seriam com `req=img`.

Especifique `text` ou omita o segundo parâmetro para retornar os dados do mapa de imagem no formato de uma sequência de elementos `HTML <AREA>` com o tipo MIME de resposta `text/plain`.

Especifique `xml` para formatar a resposta como XML em vez de HTML. A codificação de texto pode ser especificada opcionalmente. O padrão é `UTF-8`.

Retorna uma string vazia (ou elemento `<AREA>` vazio) se nenhum dado de mapa foi encontrado para os objetos de catálogo especificados e/ou se nenhum elemento `<AREA>` permanecer após o corte das imagens.

A resposta HTTP pode ser armazenada em cache com o TTL baseado em `catalog::Expiration`.

As solicitações que oferecem suporte ao formato de resposta JSONP permitem especificar o nome do manipulador de retorno de chamada JS usando a sintaxe estendida do parâmetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` é o nome do manipulador JS presente na resposta JSONP. Somente caracteres a-z, A-Z e 0-9 são permitidos. Opcional. O padrão é `s7jsonResponse`.

Consulte [Mapas de imagem](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
