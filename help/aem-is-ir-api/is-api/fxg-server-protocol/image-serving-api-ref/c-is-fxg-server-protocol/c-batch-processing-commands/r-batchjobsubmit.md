---
description: Submeta um novo trabalho em lote.
solution: Experience Manager
title: batchjobsubmit
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 0%

---


# batchjobsubmit{#batchjobsubmit}

Submeta um novo trabalho em lote.

Este parâmetro:

<table id="simpletable_11A94D630A21426F9A1CEF5EB3B9E789"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobdata  </span> </p> </td> 
  <td class="stentry"> <p>Snippet XML dos dados completos da tarefa. </p> </td> 
 </tr> 
</table>

Retorna:

<table id="simpletable_7C82E4A8520440F5A5ABBC1BCB286AB2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Status da tarefa </p> </td> 
  <td class="stentry"> <p>Se o envio foi bem-sucedido ou falhou; se bem-sucedido, ID do trabalho no formato XML. </p> </td> 
 </tr> 
</table>

## Exemplo {#section-3886e8352e26419c97b24df21ca7f6fd}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobsubmit&jobdata=<URLEncodedXMLFileContents>`
