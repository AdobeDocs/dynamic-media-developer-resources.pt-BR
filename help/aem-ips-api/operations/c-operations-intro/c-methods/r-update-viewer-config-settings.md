---
description: Atualiza as configurações do visualizador SWF.
seo-description: Atualiza as configurações do visualizador SWF.
seo-title: updateViewerConfigSettings
solution: Experience Manager
title: updateViewerConfigSettings
uuid: ad4af874-5ca4-4182-868e-afa48b1cd2b6
feature: Dynamic Media Classic, SDK/API, Predefinições do visualizador
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '74'
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
