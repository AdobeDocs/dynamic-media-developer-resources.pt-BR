---
description: Descreve métodos de operações novos e alterados para a API do IPS versão 3.8.
solution: Experience Manager
title: Operações novas e modificadas
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
exl-id: 8f4fe698-afe8-4ce6-904d-42fa67dee4dd
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

---

# Operações: Novo e Modificado{#operations-new-and-modified}

Descreve métodos de operações novos e alterados para a API do IPS versão 3.8.

Sintaxe

## Novas operações {#section-64f0e4cd01154bb68c4e3e2dd8732ef5}

* `setAssetPublishState`
* `saveZoomTarget`
* `deleteZoomTarget`
* `saveImageMap`
* `deleteImageMap`
* `createImageSet`
* `getImageSetMembers`

## Operações Modificadas {#section-25eee732b69c49d0a27b1f3290f8654a}

**searchAssets**

* O parâmetro opcional `publishState` permite pesquisar no estado do ativo `MarkedForPublish/NotMarkedForPublish`.

**getJobLogs**

* O parâmetro opcional `userHandle` permite recuperar registros de tarefas enviados por um usuário específico.
