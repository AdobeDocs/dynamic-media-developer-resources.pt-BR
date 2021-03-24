---
description: Apenas para uso interno. Consulte a seção Atributos do catálogo de referência do material de renderização de imagens .
solution: Experience Manager
title: getImageRenderingPublishSettings
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---


# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

Apenas para uso interno. Consulte a seção Atributos do catálogo de referência do material de renderização de imagens .

Sintaxe

## Tipos de usuário autorizados {#section-1097e0563c61480a8e97822dc3527070}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-4f2cb8c589384816bb2525654ec49963}

**Entrada (getImageRenderingPublishSettingsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa cujas configurações de publicação de renderização de imagem você deseja obter. |
| `*`contextHandle`*` | `xsd:string` | Sim | Lidar com o contexto de publicação. |

**Saída (getImageRenderingPublishSettingsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`publishSettingsArray`*` | `type:ConfigSettingArray` | Sim | Configurações de publicação da renderização da imagem. |

