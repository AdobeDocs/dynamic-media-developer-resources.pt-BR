---
description: Somente para uso interno. Os usuários devem consultar a seção Referência do catálogo de imagens do servidor de imagens - Referência do atributo.
solution: Experience Manager
title: getImageServingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab7b5df6-58fb-4111-be9c-76901534d167
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# getImageServingPublishSettings{#getimageservingpublishsettings}

Somente para uso interno. Os usuários devem consultar a seção Referência do catálogo de imagens do servidor de imagens - Referência do atributo.

Sintaxe

## Tipos de usuário autorizados {#section-49b7b277ba1748499121a0e90996458c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-79f0d54acd604ad2a5c96679334f2424}

**Entrada (getImageServingPublishSettingsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | O identificador da empresa com as configurações de publicação do servidor de imagens. |
| contextHandle | `xsd:string` | Sim | Processe o contexto de publicação. |

**Saída**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| publishSettingArray | `xsd:string` | Sim | Matriz de configurações de publicação do servidor de imagens. |
