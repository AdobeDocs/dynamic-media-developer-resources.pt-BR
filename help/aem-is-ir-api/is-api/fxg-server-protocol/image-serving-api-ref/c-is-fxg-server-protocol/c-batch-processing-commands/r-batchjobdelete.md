---
description: Exclua a saída de um trabalho.
seo-description: Exclua a saída de um trabalho.
seo-title: batchjobdelete
solution: Experience Manager
title: batchjobdelete
uuid: d19ed1c8-e13b-4da4-90e3-6bb0dcce2a12
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# batchjobdelete{#batchjobdelete}

Exclua a saída de um trabalho.

Se um trabalho estiver em execução no momento, ele será interrompido imediatamente e todas as suas informações de processamento serão excluídas. Se o trabalho tiver sido concluído com êxito, seu arquivo de saída será excluído.

Este parâmetro:

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> jobid</span> </p> </td> 
  <td class="stentry"> <p>ID do trabalho obtida no momento do envio. </p></td> 
 </tr> 
</table>

Retorna:

Status do trabalho no momento em que a solicitação de exclusão foi recebida, erro se `jobid` for inválido ou o trabalho já tiver sido excluído.

## Exemplo {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5]
