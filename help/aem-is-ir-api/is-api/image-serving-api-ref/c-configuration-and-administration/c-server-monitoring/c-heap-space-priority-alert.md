---
description: Um alerta de prioridade é enviado quando o espaço livre do Java heap está abaixo do limite especificado imediatamente após um ciclo de coleta de lixo Java.
seo-description: Um alerta de prioridade é enviado quando o espaço livre do Java heap está abaixo do limite especificado imediatamente após um ciclo de coleta de lixo Java.
seo-title: Alerta de prioridade do espaço de pilha
solution: Experience Manager
title: Alerta de prioridade do espaço de pilha
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 89956ad3-8a73-40db-92bd-326e3fab37ee
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---


# Alerta de prioridade do espaço de pilha{#heap-space-priority-alert}

Um alerta de prioridade é enviado quando o espaço livre do Java heap está abaixo do limite especificado imediatamente após um ciclo de coleta de lixo Java.

Alertas repetidos devem ser abordados aumentando o espaço do heap do Java. As ocorrências subsequentes desta condição não resultam em um alerta de email até que o período de atraso especificado com `AS::monitorAlertGenerator.heapSpaceResetInterval` tenha expirado.
