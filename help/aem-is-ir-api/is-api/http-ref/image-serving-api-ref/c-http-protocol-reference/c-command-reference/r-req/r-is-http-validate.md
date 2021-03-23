---
description: Solicitar validação.
seo-description: Solicitar validação.
seo-title: validate
solution: Experience Manager
title: validate
uuid: 5322c484-2cf5-4022-9863-73fc525beb56
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '112'
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
