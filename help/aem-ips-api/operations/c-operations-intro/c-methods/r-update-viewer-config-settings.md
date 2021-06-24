---
description: Atualiza as configurações do visualizador SWF.
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic, SDK/API, Predefinições do visualizador
role: Developer,Administrator
exl-id: 04565e2b-bda3-4ad0-afc1-2df01e455490
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 0%

---

# updateViewerConfigSettings{#updateviewerconfigsettings}

Atualiza as configurações do visualizador SWF.

Sintaxe

## Tipos de usuário autorizados {#section-0dd001da1b784aefa5eb5b50c7a2c045}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-29790d933fb24aa392d0cb2d52d1310f}

**Entrada (updateViewerConfigSettingsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | Manipule a empresa. |
| `*`assetHandle`*` | `xsd:string` | Sim | Identificador de ativo. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | Sim | Matriz de configurações que você deseja aplicar ao visualizador. |

**Saída (updateViewerConfigSettingsReturn)**

A API do IPS não retorna uma resposta para esta operação.
