---
description: Exclua a saída de um trabalho.
seo-description: Exclua a saída de um trabalho.
seo-title: batchjobdelete
solution: Experience Manager
title: batchjobdelete
topic: Scene7 Image Serving - Image Rendering API
uuid: d19ed1c8-e13b-4da4-90e3-6bb0dcce2a12
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# batchjobdelete{#batchjobdelete}

Exclua a saída de um trabalho.

Se um trabalho estiver sendo executado no momento, ele será interrompido imediatamente e todas as suas informações de processamento serão excluídas. Se o trabalho tiver sido concluído com êxito, seu arquivo de saída será excluído.

Este parâmetro:

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> jobid</span> </p> </td> 
  <td class="stentry"> <p>ID do trabalho obtida no momento do envio. </p></td> 
 </tr> 
</table>

Retorna:

Status do trabalho no momento em que a solicitação de exclusão foi recebida, erro se `jobid` for inválido ou se o trabalho já tiver sido excluído.

## Example {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5]
