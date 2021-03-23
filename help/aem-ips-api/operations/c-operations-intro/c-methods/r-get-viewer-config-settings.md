---
description: Obtém todas as configurações do visualizador associadas ao ativo especificado.
seo-description: Obtém todas as configurações do visualizador associadas ao ativo especificado.
seo-title: getViewerConfigSettings
solution: Experience Manager
title: getViewerConfigSettings
uuid: 61fe16de-ac72-472b-8945-f1ebe8b4d11c
feature: Dynamic Media Classic, SDK/API, Predefinições do visualizador
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '88'
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

