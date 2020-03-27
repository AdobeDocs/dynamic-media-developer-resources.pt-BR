---
description: Descreve métodos de operações novos e alterados para a API IPS versão 3.7.
seo-description: Descreve métodos de operações novos e alterados para a API IPS versão 3.7.
seo-title: Operações Novas e Modificadas
solution: Experience Manager
title: Operações Novas e Modificadas
topic: Scene7 Image Production System API
uuid: 3c163157-cd0d-4887-a1f0-7941d96c36f9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Operações: Novo e modificado{#operations-new-and-modified}

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

* Parâmetro removido `name` .
* Adicionado `excludeFieldArray`.

**getFolders**

* Adicionado `excludeFieldArray`.

**getFolderTree**

* Adicionado `excludeFieldArray` e `getUniqueMetadataValues`.
* Foi feito `fieldHandle` um parâmetro obrigatório.

