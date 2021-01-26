---
description: Apenas para uso interno. Os usuários devem consultar a seção Referência do catálogo de disponibilização de imagem - Referência do atributo.
seo-description: Apenas para uso interno. Os usuários devem consultar a seção Referência do catálogo de disponibilização de imagem - Referência do atributo.
seo-title: getImageServingPublishSettings
solution: Experience Manager
title: getImageServingPublishSettings
topic: Dynamic Media Image Production System API
uuid: 2f00198d-0262-430b-8ac5-80f52adcff67
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---


# getImageServingPublishSettings{#getimageservingpublishsettings}

Apenas para uso interno. Os usuários devem consultar a seção Referência do catálogo de disponibilização de imagem - Referência do atributo.

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
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador para a empresa com as configurações de publicação do serviço de imagem. |
| `*`contextHandle`*` | `xsd:string` | Sim | Lidar com o contexto de publicação. |

**Saída**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`publishSettingArray`*` | `xsd:string` | Sim | Configurações de publicação da matriz do servidor de imagens. |

