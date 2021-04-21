---
description: Dados do conjunto de imagens do catálogo de imagens. Retorna dados do conjunto de imagens para a entrada do catálogo de imagens especificado no caminho do URL.
solution: Experience Manager
title: imageset
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---


# imageset{#imageset}

Dados do conjunto de imagens do catálogo de imagens. Retorna dados do conjunto de imagens para a entrada do catálogo de imagens especificado no caminho do URL.

`req=imageset[,text|javascript|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> codificação</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>Identificador de solicitação exclusivo. </p></td> 
 </tr> 
</table>

O conteúdo de `catalog::ImageSet` é retornado sem qualquer modificação adicional (exceto a localização da string, se aplicável), seguida por um terminador de linha única (CR/LF). Se o caminho do URL não for resolvido para uma entrada de catálogo válida, a resposta será composta apenas de um terminador de linha único.

Outros comandos na cadeia de caracteres de solicitação são ignorados. A resposta HTTP pode ser armazenada em cache com o TTL baseado em `catalog::NonImgExpiration`.

As solicitações que oferecem suporte ao formato de resposta JSONP permitem especificar o nome do manipulador de retorno de chamada JS usando a sintaxe estendida do parâmetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` é o nome do manipulador JS presente na resposta JSONP. Somente caracteres a-z, A-Z e 0-9 são permitidos. Opcional. O padrão é `s7jsonResponse`.
