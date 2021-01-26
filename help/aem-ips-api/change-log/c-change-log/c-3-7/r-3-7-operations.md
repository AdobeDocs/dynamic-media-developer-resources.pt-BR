---
description: Descreve métodos de operações novos e alterados para a API IPS versão 3.7.
solution: Experience Manager
title: Operações Novas e Modificadas
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 0%

---


# Operações: Novo e Modificado{#operations-new-and-modified}

Descreve métodos de operações novos e alterados para a API IPS versão 3.7.

Sintaxe

## Novas Operações {#section-c4d34a58f8194d548fbe26ab3764ea58}

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

* Foi removido o parâmetro `name`.
* Adicionado `excludeFieldArray`.

**getFolders**

* Adicionado `excludeFieldArray`.

**getFolderTree**

* Adicionados `excludeFieldArray` e `getUniqueMetadataValues`.
* `fieldHandle` tornou-se um parâmetro obrigatório.

