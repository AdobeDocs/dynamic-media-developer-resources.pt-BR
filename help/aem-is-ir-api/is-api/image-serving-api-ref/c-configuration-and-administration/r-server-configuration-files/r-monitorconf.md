---
description: Contém configurações para o sistema de monitoramento/alerta.
solution: Experience Manager
title: monitor.conf
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 09c30680-dd9f-4744-b5ec-105721058883
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# monitor.conf{#monitor-conf}

Contém configurações para o sistema de monitoramento/alerta.

Esse arquivo é um arquivo de propriedades JAVA. Devem ser tomadas precauções para seguir as convenções adequadas; caso contrário, o servidor da plataforma poderá não ser iniciado. Observe, especialmente, que uma barra invertida dupla &#39;\&#39; ou uma barra invertida única &#39;/&#39; deve ser usada em vez de uma barra invertida &#39;\&#39; em caminhos de arquivo do Windows, já que a barra invertida é usada como um caractere de escape nesse tipo de arquivo.

As alterações nesse arquivo entrarão em vigor logo após o arquivo ser salvo.

<table id="simpletable_91557E1162FF4FEC8BE1722D6656CFEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Geral </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> monitorAlertGenerator.enableGlobalAlerting=false  </span> </p> <p> <span class="codeph"> mailSender.host=127.0.0.1  </span> </p> <p> <span class="codeph"> mailSender.port=25  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.messageTo=noone@scene7.com  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.messageFrom=noone@scene7.com  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.alertInterval=600000  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.heapSpaceResetInterval=600000  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.minTrafficForAlerts=0.0  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Limites de Alerta </p> </td> 
  <td class="stentry"> <p> monitorAlertGenerator.maxAverageResponseTime=200 </p> <p> monitorAlertGenerator.maxErrorRate=0.05 </p> <p> monitorAlertGenerator.minRequestRate=0.0 </p> <p> monitorAlertGenerator.minFreeHeapSpace=52428800 </p> <p> monitorAlertGenerator.maxOverlap=20 </p> <p> monitorAlertGenerator.lockedThreshold=60000 </p> </td> 
 </tr> 
</table>
