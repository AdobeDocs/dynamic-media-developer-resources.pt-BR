---
description: Atualiza as configurações do visualizador SWF.
seo-description: Atualiza as configurações do visualizador SWF.
seo-title: updateViewerConfigSettings
solution: Experience Manager
title: updateViewerConfigSettings
topic: Dynamic Media Image Production System API
uuid: ad4af874-5ca4-4182-868e-afa48b1cd2b6
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '65'
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
| `*`companyHandle`*` | `xsd:string` | Sim | Segure a empresa. |
| `*`assetHandle`*` | `xsd:string` | Sim | Identificador de ativos. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | Sim | Matriz de configurações que você deseja aplicar ao visualizador. |

**Saída (updateViewerConfigSettingsReturn)**

A API IPS não retorna uma resposta para esta operação.
