---
description: Dados do conjunto de imagens do catálogo de imagens. Retorna dados do conjunto de imagens para a entrada do catálogo de imagens especificada no caminho do URL.
seo-description: Dados do conjunto de imagens do catálogo de imagens. Retorna dados do conjunto de imagens para a entrada do catálogo de imagens especificada no caminho do URL.
seo-title: imageset
solution: Experience Manager
title: imageset
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 8854e903-a85f-403a-ae3d-b7281a236262
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---


# imageset{#imageset}

Dados do conjunto de imagens do catálogo de imagens. Retorna dados do conjunto de imagens para a entrada do catálogo de imagens especificada no caminho do URL.

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

O conteúdo de `catalog::ImageSet` é retornado sem modificações adicionais (exceto localização de string, se aplicável), seguido por um terminador de linha única (CR/LF). Se o caminho do URL não for resolvido para uma entrada de catálogo válida, a resposta será composta apenas por um terminador de linha.

Outros comandos na string de solicitação são ignorados. A resposta HTTP pode ser armazenada em cache com o TTL baseado em `catalog::NonImgExpiration`.

As solicitações compatíveis com o formato de resposta JSONP permitem que você especifique o nome do manipulador de retorno de chamada JS usando a sintaxe estendida do parâmetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` é o nome do manipulador JS presente na resposta JSONP. Somente caracteres a-z, A-Z e 0-9 são permitidos. Opcional. O padrão é `s7jsonResponse`.
