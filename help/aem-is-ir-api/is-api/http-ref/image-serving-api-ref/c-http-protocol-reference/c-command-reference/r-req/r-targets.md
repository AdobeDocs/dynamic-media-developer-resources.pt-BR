---
description: O zoom direciona os dados do catálogo de imagens. Retorna os dados de destino do zoom para a entrada do catálogo de imagens especificada no caminho da URL.
solution: Experience Manager
title: targets
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58f7b1ad-8762-4d23-b320-6f69e75ecf63
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# targets{#targets}

O zoom direciona os dados do catálogo de imagens. Retorna os dados de destino do zoom para a entrada do catálogo de imagens especificada no caminho da URL.

`req=targets[,text|{xml[, *`codificação`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> codificação</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Identificador exclusivo da solicitação. </p></td> 
 </tr> 
</table>

O conteúdo de `catalog::Targets` foi retornado. Quando o formato &#39;texto&#39; é solicitado, todas as instâncias de `??` em `catalog::Targets` são substituídas por terminadores de linha, e um terminador de linha única ( `CR/LF`) é anexado ao final. Se o caminho do URL não for resolvido para uma entrada de catálogo válida, a resposta consistirá apenas em um terminador de linha única. A formatação apropriada é aplicada quando o formato &quot;xml&quot; ou &quot;json&quot; é solicitado.

Outros comandos na cadeia de caracteres de solicitação são ignorados.

A resposta HTTP pode ser armazenada em cache com o TTL com base em `catalog::Expiration`.

As solicitações que oferecem suporte ao formato de resposta JSONP permitem especificar o nome do manipulador de retorno de chamada JS usando a sintaxe estendida do parâmetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` é o nome do manipulador JS presente na resposta JSONP. Somente caracteres a-z, A-Z e 0-9 são permitidos. Opcional. O padrão é `s7jsonResponse`.
