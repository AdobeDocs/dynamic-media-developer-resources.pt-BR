---
description: Submeta um novo processo em lote.
solution: Experience Manager
title: batchjobsubmit
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ab2f6e4-cd68-4f1e-ab54-6f5e9bfc87cb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '38'
ht-degree: 0%

---

# batchjobsubmit{#batchjobsubmit}

Submeta um novo processo em lote.

Este parâmetro:

<table id="simpletable_11A94D630A21426F9A1CEF5EB3B9E789"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> dados do trabalho </span> </p> </td> 
  <td class="stentry"> <p>Trecho XML de dados de trabalho concluídos. </p> </td> 
 </tr> 
</table>

Devoluções:

<table id="simpletable_7C82E4A8520440F5A5ABBC1BCB286AB2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Status do trabalho </p> </td> 
  <td class="stentry"> <p>Se o envio foi bem-sucedido ou falhou; se for bem-sucedido, ID do trabalho no formato XML. </p> </td> 
 </tr> 
</table>

## Exemplo {#section-3886e8352e26419c97b24df21ca7f6fd}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobsubmit&jobdata=<URLEncodedXMLFileContents>`
