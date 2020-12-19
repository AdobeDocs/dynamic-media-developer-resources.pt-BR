---
description: Dados do usuário do catálogo de imagens. Retorna os dados do usuário para a entrada do catálogo de imagens especificada no caminho do url.
seo-description: Dados do usuário do catálogo de imagens. Retorna os dados do usuário para a entrada do catálogo de imagens especificada no caminho do url.
seo-title: userdata
solution: Experience Manager
title: userdata
topic: Scene7 Image Serving - Image Rendering API
uuid: 7a34adad-f1b6-45a7-94fe-1407845710e5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---


# userdata{#userdata}

Dados do usuário do catálogo de imagens. Retorna os dados do usuário para a entrada do catálogo de imagens especificada no caminho do url.

`req=userdata[,text|{xml[, *`codificação`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> codificação</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

O conteúdo de `catalog::UserData` é retornado. Quando o formato &#39;text&#39; é especificado, todas as instâncias de `??` em `catalog::UserData`são substituídas por terminadores de linha e um terminador de linha único (CR/LF) é anexado ao final. Se o caminho do URL não for resolvido para uma entrada de catálogo válida, a resposta será composta apenas por um terminador de linha. A formatação apropriada é aplicada quando o formato &#39;xml&#39; ou &#39;json&#39; é solicitado.

Outros comandos na string de solicitação são ignorados.

A resposta HTTP pode ser armazenada em cache com o TTL baseado em `catalog::Expiration`.

>[!NOTE]
>
>O caractere de dois pontos não é permitido nos nomes das chaves da propriedade userdata.

As solicitações compatíveis com o formato de resposta JSONP permitem que você especifique o nome do manipulador de retorno de chamada JS usando a sintaxe estendida do parâmetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` é o nome do manipulador JS presente na resposta JSONP. Somente caracteres a-z, A-Z e 0-9 são permitidos. Opcional. O padrão é `s7jsonResponse`.
