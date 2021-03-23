---
description: Descreve métodos de operações novos e alterados para a API do IPS versão 3.8.
seo-description: Descreve métodos de operações novos e alterados para a API do IPS versão 3.8.
seo-title: Operações novas e modificadas
solution: Experience Manager
title: Operações novas e modificadas
uuid: e836c5af-53b8-4bfa-a93a-98750cca9745
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '82'
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

