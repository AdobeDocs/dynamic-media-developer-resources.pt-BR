---
description: Recuperar o status detalhado de um trabalho enviado.
solution: Experience Manager
title: batchjobdetails status
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
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
