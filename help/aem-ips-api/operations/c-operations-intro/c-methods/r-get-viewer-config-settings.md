---
description: Obtém todas as definições de configuração do visualizador associadas ao ativo especificado.
solution: Experience Manager
title: getViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: c0438238-8aab-4478-926a-fc0e11732fc1
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 0%

---

# getViewerConfigSettings{#getviewerconfigsettings}

Obtém todas as definições de configuração do visualizador associadas ao ativo especificado.

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
| companyHandle | `xsd:string` | Sim | Processe a empresa. |
| assetHandle | `xsd:string` | Sim | Identificar o ativo. |

**Saída (getViewerConfigSettingsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| type | `xsd:string` | Sim | Tipo de visualizador ao qual as definições de configuração se aplicam. |
| configSettingsArray | `types:ConfigSettingsArray` | Sim | Matriz de definições de configuração do visualizador. |
