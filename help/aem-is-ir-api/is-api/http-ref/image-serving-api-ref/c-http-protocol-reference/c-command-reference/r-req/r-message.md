---
description: Mensagem do cliente. Fornece um mecanismo para os clientes inserirem mensagens de texto curtas no log do servidor.
seo-description: Mensagem do cliente. Fornece um mecanismo para os clientes inserirem mensagens de texto curtas no log do servidor.
seo-title: mensagem
solution: Experience Manager
title: mensagem
topic: Scene7 Image Serving - Image Rendering API
uuid: 38d6d0e7-55cf-43ea-85b7-8f4aade4208a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 0%

---


# message{#message}

Mensagem do cliente. Fornece um mecanismo para os clientes inserirem mensagens de texto curtas no log do servidor.

`req=message&message= *`string`*`

<table id="simpletable_9AF29AA336C4447BBC2FD4A7D43ED91B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> string</span> </p> </td> 
  <td class="stentry"> <p>Sequência de caracteres da mensagem. </p></td> 
 </tr> 
</table>

A resposta HTTP não pode ser armazenada em cache. Uma resposta vazia é retornada com o tipo MIME `text/plain`.
