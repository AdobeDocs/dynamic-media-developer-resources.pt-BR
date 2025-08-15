---
description: Atualiza as configurações do visualizador do SWF.
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 04565e2b-bda3-4ad0-afc1-2df01e455490
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 0%

---

# updateViewerConfigSettings{#updateviewerconfigsettings}

Atualiza as configurações do visualizador do SWF.

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
| companyHandle | `xsd:string` | Sim | Processe a empresa. |
| assetHandle | `xsd:string` | Sim | Identificador de ativo. |
| configSettingArray | `types:ConfigSettingArray` | Sim | Matriz de definições de configuração que você deseja aplicar ao visualizador. |

**Saída (updateViewerConfigSettingsReturn)**

A API do IPS não retorna uma resposta para esta operação.
