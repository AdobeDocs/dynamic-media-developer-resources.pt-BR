---
description: Recuperar o status resumido de um job enviado.
solution: Experience Manager
title: batchjobbrief
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 0%

---


# batchjobbrief{#batchjobbriefstatus}

Recuperar o status resumido de um job enviado.

Este parâmetro:

<table id="simpletable_86E581DBB352479CB4CB531434D91E83"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>ID do trabalho obtida no momento do envio. </p> </td> 
 </tr> 
</table>

Retorna:

Breve status da tarefa no formato XML; erro se o jobid for inválido ou o trabalho tiver sido excluído.

## Exemplo {#section-806460949bb043438ad4dd4e7ab74145}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobbriefstatus&jobid=1005907604914d8eb63126b98f7172n76a5]
