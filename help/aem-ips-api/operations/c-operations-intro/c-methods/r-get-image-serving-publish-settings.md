---
description: Apenas para uso interno. Os usuários devem consultar a seção Referência do catálogo de imagem do fornecimento de imagens - Referência de atributos.
seo-description: Apenas para uso interno. Os usuários devem consultar a seção Referência do catálogo de imagem do fornecimento de imagens - Referência de atributos.
seo-title: getImageServingPublishSettings
solution: Experience Manager
title: getImageServingPublishSettings
uuid: 2f00198d-0262-430b-8ac5-80f52adcff67
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# getImageServingPublishSettings{#getimageservingpublishsettings}

Apenas para uso interno. Os usuários devem consultar a seção Referência do catálogo de imagem do fornecimento de imagens - Referência de atributos.

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
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador para a empresa com as configurações de publicação da veiculação de imagens. |
| `*`contextHandle`*` | `xsd:string` | Sim | Lidar com o contexto de publicação. |

**Saída**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`publishSettingArray`*` | `xsd:string` | Sim | Matriz de configurações de publicação do servidor de imagem. |

