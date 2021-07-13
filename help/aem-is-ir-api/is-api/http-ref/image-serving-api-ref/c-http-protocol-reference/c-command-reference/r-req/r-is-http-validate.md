---
description: Solicitar validação.
solution: Experience Manager
title: validate
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 88424371-45a0-43bb-af49-2e8568b7b44c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---

# validate{#validate}

Solicitar validação.

`req=validate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_F214CDA7580A46C0B5CF14CF13AA9B0A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span> </span> </p> </td> 
  <td class="stentry"> <p>Identificador de solicitação exclusivo. </p></td> 
 </tr> 
</table>

Analisa a cadeia de caracteres da solicitação como se `req=img` tivesse sido especificado, mas sem substituir variáveis e avaliar objetos referenciados (imagens, perfis ICC, fontes e assim por diante). A resposta de erro padrão é retornada se a análise falhar, caso contrário, a seguinte propriedade é retornada:

`request.isValid=1`

A resposta HTTP não pode ser armazenada em cache.

As solicitações que oferecem suporte ao formato de resposta JSONP permitem especificar o nome do manipulador de retorno de chamada JS usando a sintaxe estendida do parâmetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` é o nome do manipulador JS presente na resposta JSONP. Somente caracteres a-z, A-Z e 0-9 são permitidos. Opcional. O padrão é `s7jsonResponse`.
