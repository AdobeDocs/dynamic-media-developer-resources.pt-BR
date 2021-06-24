---
description: Um alerta de prioridade é enviado quando o espaço livre de heap do Java está abaixo do limite especificado imediatamente após um ciclo de coleta de lixo do Java.
solution: Experience Manager
title: Alerta de prioridade de espaço de heap
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 32951003-386f-4ea2-a5a0-f4d2e6d95ba5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# Alerta de prioridade de espaço de heap{#heap-space-priority-alert}

Um alerta de prioridade é enviado quando o espaço livre de heap do Java está abaixo do limite especificado imediatamente após um ciclo de coleta de lixo do Java.

Alertas repetidos devem ser abordados com o aumento do espaço de heap do Java. As ocorrências subsequentes dessa condição não resultam em um alerta por email até que o período de atraso especificado com `AS::monitorAlertGenerator.heapSpaceResetInterval` tenha expirado.
