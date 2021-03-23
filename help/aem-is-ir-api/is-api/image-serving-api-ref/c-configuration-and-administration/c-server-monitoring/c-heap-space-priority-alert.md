---
description: Um alerta de prioridade é enviado quando o espaço livre de heap do Java está abaixo do limite especificado imediatamente após um ciclo de coleta de lixo do Java.
seo-description: Um alerta de prioridade é enviado quando o espaço livre de heap do Java está abaixo do limite especificado imediatamente após um ciclo de coleta de lixo do Java.
seo-title: Alerta de prioridade de espaço de heap
solution: Experience Manager
title: Alerta de prioridade de espaço de heap
uuid: 89956ad3-8a73-40db-92bd-326e3fab37ee
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# Alerta de prioridade de espaço de heap{#heap-space-priority-alert}

Um alerta de prioridade é enviado quando o espaço livre de heap do Java está abaixo do limite especificado imediatamente após um ciclo de coleta de lixo do Java.

Alertas repetidos devem ser abordados com o aumento do espaço de heap do Java. As ocorrências subsequentes dessa condição não resultam em um alerta por email até que o período de atraso especificado com `AS::monitorAlertGenerator.heapSpaceResetInterval` tenha expirado.
