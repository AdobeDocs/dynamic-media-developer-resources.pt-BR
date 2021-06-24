---
description: Informações do conjunto de mídia.
solution: Experience Manager
title: set
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: bc69f094-ff21-4dd7-9e10-daddb3de0c65
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# set{#set}

Informações do conjunto de mídia.

req=set[,xml[, *`encoding`*]|{json[&amp;id=*`reqId`*]}]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> codificação</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>Identificador de solicitação único </p></td> 
 </tr> 
</table>

Retorna informações sobre imagens, vídeos, amostras e vários metadados associados a catalog::ImageSet para a entrada de catálogo de imagem especificada no caminho do URL. Essa resposta é uma estrutura hierárquica, determinada pelo tipo de conjunto fornecido. A formatação apropriada é aplicada quando o formato &#39;xml&#39; ou &#39;json&#39; é solicitado.

A resposta HTTP pode ser armazenada em cache com o TTL baseado em `catalog::NonImgExpiration`.

>[!NOTE]
>
>O caractere de dois pontos não é permitido em solicitações req=set.

As solicitações que oferecem suporte ao formato de resposta JSON permitem especificar o nome do manipulador de retorno de chamada JS usando a sintaxe estendida do parâmetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` é o nome do manipulador JS presente na resposta JSONP. Somente caracteres a-z, A-Z e 0-9 são permitidos. Opcional. O padrão é `s7jsonResponse`.
