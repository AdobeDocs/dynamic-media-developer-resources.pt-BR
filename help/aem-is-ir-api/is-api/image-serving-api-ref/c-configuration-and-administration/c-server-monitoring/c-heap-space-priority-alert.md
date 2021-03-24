---
description: Um alerta de prioridade é enviado quando o espaço livre de heap do Java está abaixo do limite especificado imediatamente após um ciclo de coleta de lixo do Java.
solution: Experience Manager
title: Alerta de prioridade de espaço de heap
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# Alerta de prioridade de espaço de heap{#heap-space-priority-alert}

Um alerta de prioridade é enviado quando o espaço livre de heap do Java está abaixo do limite especificado imediatamente após um ciclo de coleta de lixo do Java.

Alertas repetidos devem ser abordados com o aumento do espaço de heap do Java. As ocorrências subsequentes dessa condição não resultam em um alerta por email até que o período de atraso especificado com `AS::monitorAlertGenerator.heapSpaceResetInterval` tenha expirado.
