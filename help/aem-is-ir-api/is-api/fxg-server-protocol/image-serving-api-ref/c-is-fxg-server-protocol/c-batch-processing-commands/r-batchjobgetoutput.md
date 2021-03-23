---
description: Recupere a saída de um trabalho enviado.
seo-description: Recupere a saída de um trabalho enviado.
seo-title: batchjobgetoutput
solution: Experience Manager
title: batchjobgetoutput
uuid: c2d49cc2-3223-4f0f-8ba7-4f74a5f76789
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 0%

---


# batchjobgetoutput{#batchjobgetoutput}

Recupere a saída de um trabalho enviado.

Este parâmetro:

<table id="simpletable_D8AA325968AD4FAEA7B214F0CBBF3F08"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>ID do trabalho obtida no momento do envio. </p> </td> 
 </tr> 
</table>

Retorna:

A saída em PDF da tarefa é transmitida em resposta; erro se `jobid` for inválido ou se o trabalho tiver sido excluído.

## Exemplo {#section-0319e615fa254132a9dab59351b4c252}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobgetoutput&jobid=1005907604914d8eb63126b98f7172n76a5]
