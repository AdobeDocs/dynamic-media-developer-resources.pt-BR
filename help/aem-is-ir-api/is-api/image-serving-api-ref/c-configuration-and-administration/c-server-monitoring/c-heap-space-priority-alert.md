---
description: Um alerta de prioridade é enviado quando o espaço livre do heap de Java está abaixo do limite especificado imediatamente após um ciclo de coleta de lixo Java.
solution: Experience Manager
title: Alerta de prioridade de espaço de heap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 32951003-386f-4ea2-a5a0-f4d2e6d95ba5
TQID: 'https://experienceleague.adobe.com/zCx9aodQa-gcTc0iFuK3N0fJf43EdyCWk8cYIawYPaM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 85
ht-degree: 0%

---

# Alerta de prioridade de espaço de heap{#heap-space-priority-alert}

Um alerta de prioridade é enviado quando o espaço livre do heap de Java está abaixo do limite especificado imediatamente após um ciclo de coleta de lixo Java.

Os alertas repetidos devem ser abordados aumentando o espaço do heap Java. Ocorrências subsequentes dessa condição não resultarão em um alerta por email até que o período de atraso especificado com `AS::monitorAlertGenerator.heapSpaceResetInterval` tenha expirado.
