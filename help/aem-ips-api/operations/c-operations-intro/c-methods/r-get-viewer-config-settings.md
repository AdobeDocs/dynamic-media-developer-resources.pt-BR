---
description: Obtém todas as configurações do visualizador associadas ao ativo especificado.
seo-description: Obtém todas as configurações do visualizador associadas ao ativo especificado.
seo-title: getViewerConfigSettings
solution: Experience Manager
title: getViewerConfigSettings
topic: Dynamic Media Image Production System API
uuid: 61fe16de-ac72-472b-8945-f1ebe8b4d11c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '79'
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
| `*`companyHandle`*` | `xsd:string` | Sim | Segure a empresa. |
| `*`assetHandle`*` | `xsd:string` | Sim | Lidar com o ativo. |

**Saída (getViewerCoinfigSettingsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`type`*` | `xsd:string` | Sim | Tipo de visualizador ao qual as configurações se aplicam. |
| `*`configSettingsArray`*` | `types:ConfigSettingsArray` | Sim | Matriz de configurações do visualizador. |

