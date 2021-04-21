---
description: Recuperar o status detalhado de um trabalho enviado.
solution: Experience Manager
title: batchjobdetails status
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 0%

---


# batchjobdetaledstatus{#batchjobdetailedstatus}

Recuperar o status detalhado de um trabalho enviado.

Este parâmetro:

<table id="simpletable_9C379451927C4058834640377C0BD7A0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>ID do trabalho obtida no momento do envio. </p> </td> 
 </tr> 
</table>

Retorna:

Status detalhado da tarefa no formato XML; erro se `jobid` for inválido ou se o trabalho tiver sido excluído.

## Exemplo {#section-55f463750afe4814b5fdbaa2f1aafab4}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdetailedstatus&jobid=1005907604914d8eb63126b98f7172n76a5`
