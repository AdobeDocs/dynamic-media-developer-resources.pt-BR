---
description: Mensagem do cliente. Fornece um mecanismo para os clientes inserirem mensagens de texto curtas no registro do servidor.
solution: Experience Manager
title: mensagem
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 47e51181-714c-4b25-a375-f3b2238cd534
TQID: 'https://experienceleague.adobe.com/LmWXluV-uBCDX7ip4mUDsmlknIT8SPQmnF4aOYd89s8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 52
ht-degree: 0%

---

# mensagem{#message}

Mensagem do cliente. Fornece um mecanismo para os clientes inserirem mensagens de texto curtas no registro do servidor.

`req=message&message= *`cadeia de caracteres`*`

<table id="simpletable_9AF29AA336C4447BBC2FD4A7D43ED91B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cadeia de caracteres</span> </p> </td> 
  <td class="stentry"> <p>String de mensagem. </p></td> 
 </tr> 
</table>

A resposta HTTP não pode ser armazenada em cache. Uma resposta vazia é retornada com o tipo MIME `text/plain`.
