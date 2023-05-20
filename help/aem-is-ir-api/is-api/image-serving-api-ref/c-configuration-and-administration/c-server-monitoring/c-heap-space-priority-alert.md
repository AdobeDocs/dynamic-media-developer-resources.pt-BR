---
description: Um alerta de prioridade é enviado quando o espaço livre do heap de Java está abaixo do limite especificado imediatamente após um ciclo de coleta de lixo Java.
solution: Experience Manager
title: Alerta de prioridade de espaço de heap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 32951003-386f-4ea2-a5a0-f4d2e6d95ba5
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---

# Alerta de prioridade de espaço de heap{#heap-space-priority-alert}

Um alerta de prioridade é enviado quando o espaço livre do heap de Java está abaixo do limite especificado imediatamente após um ciclo de coleta de lixo Java.

Os alertas repetidos devem ser abordados aumentando o espaço do heap Java. Ocorrências subsequentes dessa condição não resultarão em um alerta por email até o período de atraso especificado com `AS::monitorAlertGenerator.heapSpaceResetInterval` expirou.
