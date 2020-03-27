---
description: Recuperar a saída de uma tarefa submetida.
seo-description: Recuperar a saída de uma tarefa submetida.
seo-title: batchjobgetoutput
solution: Experience Manager
title: batchjobgetoutput
topic: Scene7 Image Serving - Image Rendering API
uuid: c2d49cc2-3223-4f0f-8ba7-4f74a5f76789
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# batchjobgetoutput{#batchjobgetoutput}

Recuperar a saída de uma tarefa submetida.

Este parâmetro:

<table id="simpletable_D8AA325968AD4FAEA7B214F0CBBF3F08"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid </span> </p> </td> 
  <td class="stentry"> <p>ID do trabalho obtida no momento do envio. </p> </td> 
 </tr> 
</table>

Retorna:

A saída PDF da tarefa é transmitida em sequência; erro se `jobid` for inválido ou se o trabalho tiver sido excluído.

## Example {#section-0319e615fa254132a9dab59351b4c252}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobgetoutput&jobid=1005907604914d8eb63126b98f7172n76a5]
