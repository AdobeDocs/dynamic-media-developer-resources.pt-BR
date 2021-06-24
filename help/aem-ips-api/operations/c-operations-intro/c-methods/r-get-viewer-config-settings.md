---
description: Obtém todas as configurações do visualizador associadas ao ativo especificado.
solution: Experience Manager
title: getViewerConfigSettings
feature: Dynamic Media Classic, SDK/API, Predefinições do visualizador
role: Developer,Administrator
exl-id: c0438238-8aab-4478-926a-fc0e11732fc1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---

# getViewerConfigSettings{#getviewerconfigsettings}

Obtém todas as configurações do visualizador associadas ao ativo especificado.

Sintaxe

## Tipos de usuário autorizados {#section-05c3ea8f7d2d42c6bf7af63e03f457a9}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-7d06abf3d707494c8a1270c7fa1477f1}

**Entrada (getViewerConfigSettingsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | Manipule a empresa. |
| `*`assetHandle`*` | `xsd:string` | Sim | Lidar com o ativo. |

**Saída (getViewerCoinfigSettingsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`type`*` | `xsd:string` | Sim | Tipo de visualizador ao qual as configurações se aplicam. |
| `*`configSettingsArray`*` | `types:ConfigSettingsArray` | Sim | Matriz de configurações do visualizador. |
