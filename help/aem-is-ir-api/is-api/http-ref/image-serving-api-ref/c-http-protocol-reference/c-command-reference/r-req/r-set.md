---
description: Informações do conjunto de mídias.
solution: Experience Manager
title: set
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bc69f094-ff21-4dd7-9e10-daddb3de0c65
TQID: 'https://experienceleague.adobe.com/nfNdFeRk7TDhSYHdy05x6fxNKMBhTF7f11xoji13VP4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 144
ht-degree: 0%

---

# set{#set}

Informações do conjunto de mídias.

req=set[,xml[, *`encoding`*]|&lbrace;json[&amp;id=*`reqId`*]]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> codificação</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>Identificador exclusivo da solicitação </p></td> 
 </tr> 
</table>

Retorna informações sobre imagens, vídeos, amostras e vários metadados associados a catalog::ImageSet para a entrada do catálogo de imagens especificada no caminho do URL. Essa resposta é uma estrutura hierárquica conforme determinado pelo tipo de conjunto fornecido. A formatação apropriada é aplicada quando o formato &quot;xml&quot; ou &quot;json&quot; é solicitado.

A resposta HTTP pode ser armazenada em cache com o TTL com base em `catalog::NonImgExpiration`.

>[!NOTE]
>
>O caractere dois pontos não é permitido em solicitações req=set.

As solicitações que oferecem suporte ao formato de resposta JSON permitem especificar o nome do manipulador de retorno de chamada JS usando a sintaxe estendida do parâmetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` é o nome do manipulador JS presente na resposta JSONP. Somente caracteres a-z, A-Z e 0-9 são permitidos. Opcional. O padrão é `s7jsonResponse`.
