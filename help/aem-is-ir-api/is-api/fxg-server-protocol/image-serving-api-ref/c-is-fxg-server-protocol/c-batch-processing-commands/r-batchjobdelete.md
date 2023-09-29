---
title: batchjobdelete
description: Deletar a saída de um job.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9aca6693-32ac-4abd-9595-95bce60050ec
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---

# batchjobdelete{#batchjobdelete}

Deletar a saída de um job.

Se um job estiver sendo executado no momento, ele será interrompido imediatamente e todas as suas informações de processamento serão excluídas. Se o trabalho tiver sido concluído com êxito, seu arquivo de saída será excluído.

Este parâmetro:

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> job_id</span> </p> </td> 
  <td class="stentry"> <p>A ID do trabalho obtida no momento do envio. </p></td> 
 </tr> 
</table>

Devoluções:

Status do trabalho no momento em que a solicitação de exclusão foi recebida; erro se `jobid` é inválido ou o trabalho já foi excluído.

## Exemplo {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5`
