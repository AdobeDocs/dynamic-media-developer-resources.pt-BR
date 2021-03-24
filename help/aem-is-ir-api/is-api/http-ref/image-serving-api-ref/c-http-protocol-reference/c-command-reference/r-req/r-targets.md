---
description: O zoom segmenta os dados do catálogo de imagens. Retorna dados de destino de zoom para a entrada do catálogo de imagens especificada no caminho do URL.
solution: Experience Manager
title: targets
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---


# targets{#targets}

O zoom segmenta os dados do catálogo de imagens. Retorna dados de destino de zoom para a entrada do catálogo de imagens especificada no caminho do URL.

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

O conteúdo de `catalog::Targets` é retornado. Quando o formato &#39;text&#39; é solicitado, todas as instâncias de `??` em `catalog::Targets` são substituídas por terminadores de linha e um terminador de linha único ( `CR/LF`) é anexado ao final. Se o caminho do URL não for resolvido para uma entrada de catálogo válida, a resposta será composta apenas de um terminador de linha único. A formatação apropriada é aplicada quando o formato &#39;xml&#39; ou &#39;json&#39; é solicitado.

Outros comandos na cadeia de caracteres de solicitação são ignorados.

A resposta HTTP pode ser armazenada em cache com o TTL baseado em `catalog::Expiration`.

As solicitações que oferecem suporte ao formato de resposta JSONP permitem especificar o nome do manipulador de retorno de chamada JS usando a sintaxe estendida do parâmetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` é o nome do manipulador JS presente na resposta JSONP. Somente caracteres a-z, A-Z e 0-9 são permitidos. Opcional. O padrão é `s7jsonResponse`.
