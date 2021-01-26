---
description: Descreve métodos de operações novos e alterados para a API IPS versão 3.8.
seo-description: Descreve métodos de operações novos e alterados para a API IPS versão 3.8.
seo-title: Operações Novas e Modificadas
solution: Experience Manager
title: Operações Novas e Modificadas
topic: Dynamic Media Image Production System API
uuid: e836c5af-53b8-4bfa-a93a-98750cca9745
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---


# Operações: Novo e Modificado{#operations-new-and-modified}

Descreve métodos de operações novos e alterados para a API IPS versão 3.8.

Sintaxe

## Novas Operações {#section-64f0e4cd01154bb68c4e3e2dd8732ef5}

* `setAssetPublishState`
* `saveZoomTarget`
* `deleteZoomTarget`
* `saveImageMap`
* `deleteImageMap`
* `createImageSet`
* `getImageSetMembers`

## Operações Modificadas {#section-25eee732b69c49d0a27b1f3290f8654a}

**searchAssets**

* O parâmetro opcional `publishState` permite que você pesquise no estado `MarkedForPublish/NotMarkedForPublish` do ativo.

**getJobLogs**

* O parâmetro opcional `userHandle` permite que você recupere logs de tarefas enviados por um usuário específico.

