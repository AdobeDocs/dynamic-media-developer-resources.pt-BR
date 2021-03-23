---
description: Anexa as configurações do visualizador a um ativo. Pode ser uma predefinição do visualizador ou o ativo de origem do visualizador.
seo-description: Anexa as configurações do visualizador a um ativo. Pode ser uma predefinição do visualizador ou o ativo de origem do visualizador.
seo-title: setViewerConfigSettings
solution: Experience Manager
title: setViewerConfigSettings
uuid: d83d866e-9243-479f-9b33-727aad8158e5
feature: Dynamic Media Classic, SDK/API, Predefinições do visualizador
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '133'
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
