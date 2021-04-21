---
description: Anexa as configurações do visualizador a um ativo. Pode ser uma predefinição do visualizador ou o ativo de origem do visualizador.
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---


# setViewerConfigSettings{#setviewerconfigsettings}

Anexa as configurações do visualizador a um ativo. Pode ser uma predefinição do visualizador ou o ativo de origem do visualizador.

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
| `*`companyHandle`*` | `xsd:string` | Sim | Manipule a empresa. |
| `*`assetHandle`*` | `xsd:string` | Sim | Identificador de ativo. |
| `*`name`*` | `xsd:string` | Sim | Nome do ativo. |
| `*`type`*` | `xsd:string` | Sim | O tipo de ativo ao qual você deseja aplicar a configuração do visualizador. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | Sim | A matriz de `ConfigSettings` aplicada ao ativo. |

**Saída (setViewerConfigSettingsParam)**

A API do IPS não retorna uma resposta para esta operação.
