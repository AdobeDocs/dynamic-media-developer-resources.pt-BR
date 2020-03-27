---
description: Contém configurações para o sistema de monitoramento/alerta.
seo-description: Contém configurações para o sistema de monitoramento/alerta.
seo-title: monitor.conf
solution: Experience Manager
title: monitor.conf
topic: Scene7 Image Serving - Image Rendering API
uuid: 31949797-df2c-4b7c-841b-4c623299a228
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# monitor.conf{#monitor-conf}

Contém configurações para o sistema de monitoramento/alerta.

Este arquivo é um arquivo de propriedades JAVA. Devem ser tomadas precauções para seguir as convenções adequadas; caso contrário, o Servidor da plataforma poderá falhar no start. Observe especialmente que uma barra invertida de duplo &#39;\\&#39; ou uma barra invertida &#39;/&#39; deve ser usada em vez de uma barra invertida &#39;\&#39; nos caminhos de arquivos do Windows, já que a barra invertida é usada como um caractere de escape nesse tipo de arquivo.

As alterações neste arquivo entrarão em vigor logo após o arquivo ser salvo.

<table id="simpletable_91557E1162FF4FEC8BE1722D6656CFEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Geral </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> monitorAlertGenerator.enableGlobalAlerting=false </span> </p> <p> <span class="codeph"> mailSender.host=127.0.0.1 </span> </p> <p> <span class="codeph"> mailSender.port=25 </span> </p> <p> <span class="codeph"> monitorAlertGenerator.messageTo=noone@scene7.com </span> </p> <p> <span class="codeph"> monitorAlertGenerator.messageFrom=noone@scene7.com </span> </p> <p> <span class="codeph"> monitorAlertGenerator.alertInterval=600000 </span> </p> <p> <span class="codeph"> monitorAlertGenerator.heapSpaceResetInterval=600000 </span> </p> <p> <span class="codeph"> monitorAlertGenerator.minTrafficForAlerts=0.0 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Limites de Alerta </p> </td> 
  <td class="stentry"> <p> monitorAlertGenerator.maxAverageResponseTime=200 </p> <p> monitorAlertGenerator.maxErrorRate=0.05 </p> <p> monitorAlertGenerator.minRequestRate=0.0 </p> <p> monitorAlertGenerator.minFreeHeapSpace=52428800 </p> <p> monitorAlertGenerator.maxOverlap=20 </p> <p> monitorAlertGenerator.lockedThreshold=60000 </p> </td> 
 </tr> 
</table>

