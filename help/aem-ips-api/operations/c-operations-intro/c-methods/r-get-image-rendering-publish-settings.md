---
description: Apenas para uso interno. Consulte a seção Atributos do catálogo de referência do catálogo de materiais de renderização de imagens.
seo-description: Apenas para uso interno. Consulte a seção Atributos do catálogo de referência do catálogo de materiais de renderização de imagens.
seo-title: getImageRenderingPublishSettings
solution: Experience Manager
title: getImageRenderingPublishSettings
topic: Scene7 Image Production System API
uuid: b1c253b5-febe-4dc7-95a1-a5f4789030e7
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

Apenas para uso interno. Consulte a seção Atributos do catálogo de referência do catálogo de materiais de renderização de imagens.

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
| ` *`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa cujas configurações de publicação de renderização de imagem você deseja obter. |
| ` *`contextHandle`*` | `xsd:string` | Sim | Lidar com o contexto de publicação. |

**Saída (getImageRenderingPublishSettingsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| ` *`publishSettingsArray`*` | `type:ConfigSettingArray` | Sim | Configurações de publicação de renderização de imagem. |

