---
description: Dados do usuário do catálogo de imagens. Retorna os dados do usuário para a entrada do catálogo de imagens especificada no caminho da url.
solution: Experience Manager
title: userdata
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b1d85ea6-0e12-49a8-b1dc-4c64a672770b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# userdata{#userdata}

Dados do usuário do catálogo de imagens. Retorna os dados do usuário para a entrada do catálogo de imagens especificada no caminho da url.

`req=userdata[,text|{xml[, *`codificação`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> codificação</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

O conteúdo de `catalog::UserData` foi retornado. Quando o formato &#39;text&#39; é especificado, todas as instâncias de `??` em `catalog::UserData` são substituídas por terminadores de linha, e um terminador de linha única (CR/LF) é anexado ao final. Se o caminho do URL não for resolvido para uma entrada de catálogo válida, a resposta consistirá apenas em um terminador de linha única. A formatação apropriada é aplicada quando o formato &quot;xml&quot; ou &quot;json&quot; é solicitado.

Outros comandos na cadeia de caracteres de solicitação são ignorados.

A resposta HTTP pode ser armazenada em cache com o TTL com base em `catalog::Expiration`.

>[!NOTE]
>
>O caractere dois pontos não é permitido em nomes de chave de propriedade userdata.

As solicitações que oferecem suporte ao formato de resposta JSONP permitem especificar o nome do manipulador de retorno de chamada JS usando a sintaxe estendida do parâmetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` é o nome do manipulador JS presente na resposta JSONP. Somente caracteres a-z, A-Z e 0-9 são permitidos. Opcional. O padrão é `s7jsonResponse`.
