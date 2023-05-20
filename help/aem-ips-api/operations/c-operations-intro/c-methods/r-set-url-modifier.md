---
description: Define os comandos do protocolo Servidor de imagens ou Renderização de imagens para o ativo especificado. Esses comandos modificam a representação do ativo sem destruí-lo.
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9e96ffc8-5a38-46b8-9ba8-956c86b32c7a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---

# setUrlModifier{#seturlmodifier}

Define os comandos do protocolo Servidor de imagens ou Renderização de imagens para o ativo especificado. Esses comandos modificam a representação do ativo sem destruí-lo.

Para o Servidor de imagens, os comandos na `urlModifier` são publicados no campo Catálogo do modificador e aplicados antes de qualquer comando especificado no URL da solicitação. Comandos em `urlPostApplyModifier` são publicados na `PostModifier` catálogo e substituir quaisquer comandos no URL da solicitação ou no `urlModifier`. Para Renderização de imagem, os comandos em `urlModifier` e `urlPostApplyModifier` são concatenadas e publicadas no campo Modifier catalog.

## Tipos de usuário autorizados {#section-fefcd732ccf64c78956606538f96c73d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-3304fe49bbe24ea1a886e19aaf41fb7d}

**Entrada (setUrlModifierParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | Identificador da empresa. |
| assetHandle | `xsd:string` | Sim | Identificador de ativo. |
| urlModifier | `xsd:string` | Não | Comandos do protocolo Image Serving ou Image Rendering a serem aplicados antes da solicitação ou `urlPostApplyModifier` comandos. |
| urlPostApplyModifier | `xsd:string` | Não | Comandos do protocolo Image Serving ou Image Rendering a serem aplicados após `urlModifier` comandos e request. |

**Saída (setUrlModifierReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-801d4b9b986443f59a5783a3d6bf44aa}

**Solicitação**

```java
<setUrlModifierParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|942|1|579</assetHandle>
   <urlModifier>modify=that</urlModifier>
   <urlPostApplyModifier>action=awesomeToo</urlPostApplyModifier>
</setUrlModifierParam>
```

**Resposta**

Nenhum.
