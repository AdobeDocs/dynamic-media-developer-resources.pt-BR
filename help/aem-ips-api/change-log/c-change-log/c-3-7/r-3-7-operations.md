---
description: Descreve métodos de operações novos e alterados para a API do IPS versão 3.7.
solution: Experience Manager
title: Operações novas e modificadas
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 1f11a686-7239-4922-a608-5330864184ac
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 0%

---

# Operações: Novo e modificado{#operations-new-and-modified}

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

## Operações modificadas {#section-596ea55a371e4c2ab5531e21ea9d8090}

**searchAsset**

* Remoção do parâmetro `name`.
* Adição de `excludeFieldArray`.

**getFolders**

* Adição de `excludeFieldArray`.

**getFolderTree**

* Adição de `excludeFieldArray` e `getUniqueMetadataValues`.
* `fieldHandle` tornou-se um parâmetro obrigatório.
