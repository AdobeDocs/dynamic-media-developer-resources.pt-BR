---
description: Atualiza as configurações do visualizador SWF.
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic, SDK/API, Predefinições do visualizador
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '68'
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
