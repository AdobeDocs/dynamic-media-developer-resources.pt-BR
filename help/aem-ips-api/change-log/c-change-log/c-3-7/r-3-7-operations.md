---
description: Descreve métodos de operações novos e alterados para a API do IPS versão 3.7.
solution: Experience Manager
title: Operações novas e modificadas
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 0%

---


# Operações: Novo e Modificado{#operations-new-and-modified}

Descreve métodos de operações novos e alterados para a API do IPS versão 3.7.

Sintaxe

## Novas operações {#section-c4d34a58f8194d548fbe26ab3764ea58}

* `moveAsset`
* `renameAsset`
* `deleteAsset`
* `createFolder`
* `deleteFolder`
* `getActiveJobs`
* `getScheduledJobs`
* `getJobLogs`
* `getJbLogDetails`
* `submitJob`
* `stopJob`
* `pauseJob`
* `resumeJob`
* `executeJob`
* `deleteJob`

## Operações Modificadas {#section-596ea55a371e4c2ab5531e21ea9d8090}

**searchAsset**

* Remoção do parâmetro `name`.
* Adição de `excludeFieldArray`.

**getFolders**

* Adição de `excludeFieldArray`.

**getFolderTree**

* Adição de `excludeFieldArray` e `getUniqueMetadataValues`.
* `fieldHandle` tornou-se um parâmetro obrigatório.

