---
description: Zoom nos dados de públicos alvos do catálogo de imagens. Retorna os dados do público alvo de zoom para a entrada do catálogo de imagens especificada no caminho do URL.
seo-description: Zoom nos dados de públicos alvos do catálogo de imagens. Retorna os dados do público alvo de zoom para a entrada do catálogo de imagens especificada no caminho do URL.
seo-title: públicos alvos
solution: Experience Manager
title: públicos alvos
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e20dcd2c-913a-4153-97c7-dfb190763e39
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---


# públicos alvos{#targets}

Zoom nos dados de públicos alvos do catálogo de imagens. Retorna os dados do público alvo de zoom para a entrada do catálogo de imagens especificada no caminho do URL.

`req=targets[,text|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> codificação</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Identificador de solicitação exclusivo. </p></td> 
 </tr> 
</table>

O conteúdo de `catalog::Targets` é retornado. Quando o formato &#39;text&#39; é solicitado, todas as instâncias de `??` em `catalog::Targets` são substituídas por terminadores de linha e um terminador de linha único ( `CR/LF`) é anexado ao final. Se o caminho do URL não for resolvido para uma entrada de catálogo válida, a resposta será composta apenas por um terminador de linha. A formatação apropriada é aplicada quando o formato &#39;xml&#39; ou &#39;json&#39; é solicitado.

Outros comandos na string de solicitação são ignorados.

A resposta HTTP pode ser armazenada em cache com o TTL baseado em `catalog::Expiration`.

As solicitações compatíveis com o formato de resposta JSONP permitem que você especifique o nome do manipulador de retorno de chamada JS usando a sintaxe estendida do parâmetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` é o nome do manipulador JS presente na resposta JSONP. Somente caracteres a-z, A-Z e 0-9 são permitidos. Opcional. O padrão é `s7jsonResponse`.
