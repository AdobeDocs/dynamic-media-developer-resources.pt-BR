---
description: Anexa as configurações do visualizador a um ativo. Eles podem ser uma predefinição do visualizador ou o ativo de origem do visualizador.
seo-description: Anexa as configurações do visualizador a um ativo. Eles podem ser uma predefinição do visualizador ou o ativo de origem do visualizador.
seo-title: setViewerConfigSettings
solution: Experience Manager
title: setViewerConfigSettings
topic: Dynamic Media Image Production System API
uuid: d83d866e-9243-479f-9b33-727aad8158e5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# setViewerConfigSettings{#setviewerconfigsettings}

Anexa as configurações do visualizador a um ativo. Eles podem ser uma predefinição do visualizador ou o ativo de origem do visualizador.

Sintaxe

## Tipos de usuário autorizados {#section-81c429ba9f4c4359986a30ea7ebea8d2}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-bcc8c83cc84141e8b1341be9133e8511}

**Entrada (setViewerConfigSettingsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | Segure a empresa. |
| `*`assetHandle`*` | `xsd:string` | Sim | Identificador de ativos. |
| `*`name`*` | `xsd:string` | Sim | Nome do ativo. |
| `*`type`*` | `xsd:string` | Sim | O tipo de ativo ao qual você deseja aplicar a configuração do visualizador. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | Sim | A matriz de `ConfigSettings` aplicada ao ativo. |

**Saída (setViewerConfigSettingsParam)**

A API IPS não retorna uma resposta para esta operação.
