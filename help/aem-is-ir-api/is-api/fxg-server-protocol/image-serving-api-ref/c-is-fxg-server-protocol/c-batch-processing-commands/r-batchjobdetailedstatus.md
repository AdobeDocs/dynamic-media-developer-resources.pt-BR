---
description: Recuperar o status detalhado de um processo enviado.
solution: Experience Manager
title: batchjobdetailedstatus
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd385327-29af-448c-9a25-75098b578272
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 0%

---

# batchjobdetailedstatus{#batchjobdetailedstatus}

Recuperar o status detalhado de um processo enviado.

Este parâmetro:

<table id="simpletable_9C379451927C4058834640377C0BD7A0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> id do trabalho </span> </p> </td> 
  <td class="stentry"> <p>A ID do trabalho obtida no momento do envio. </p> </td> 
 </tr> 
</table>

Devoluções:

Status detalhado do trabalho no formato XML; erro se `jobid` for inválido ou se o trabalho tiver sido excluído.

## Exemplo {#section-55f463750afe4814b5fdbaa2f1aafab4}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdetailedstatus&jobid=1005907604914d8eb63126b98f7172n76a5`
