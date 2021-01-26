---
description: Define os comandos do protocolo Servidor de imagens ou Renderização de imagens para o ativo especificado. Esses comandos modificam a representação do ativo sem destruí-lo.
seo-description: Define os comandos do protocolo Servidor de imagens ou Renderização de imagens para o ativo especificado. Esses comandos modificam a representação do ativo sem destruí-lo.
seo-title: setUrlModifier
solution: Experience Manager
title: setUrlModifier
topic: Dynamic Media Image Production System API
uuid: ec423e57-338b-4a32-be5a-a73fa96712ce
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---


# setUrlModifier{#seturlmodifier}

Define os comandos do protocolo Servidor de imagens ou Renderização de imagens para o ativo especificado. Esses comandos modificam a representação do ativo sem destruí-lo.

Para o Serviço de imagem, os comandos no parâmetro `urlModifier` são publicados no campo de catálogo Modificador e aplicados antes de qualquer comando especificado no URL da solicitação. Os comandos em `urlPostApplyModifier` serão publicados no campo de catálogo `PostModifier` e substituirão quaisquer comandos no URL da solicitação ou em `urlModifier`. Para renderização de imagem, os comandos em `urlModifier` e `urlPostApplyModifier` são concatenados e publicados no campo de catálogo Modificador.

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
| `*`companyHandle`*` | `xsd:string` | Sim | Alça da empresa. |
| `*`assetHandle`*` | `xsd:string` | Sim | Identificador de ativos. |
| `*`urlModifier`*` | `xsd:string` | Não | Comandos do protocolo de disponibilização ou renderização de imagem a serem aplicados antes dos comandos request ou `urlPostApplyModifier`. |
| `*`urlPostApplyModifier`*` | `xsd:string` | Não | Comandos do protocolo de disponibilização ou renderização de imagem a serem aplicados após `urlModifier` e solicitar comandos. |

**Saída (setUrlModifierReturn)**

A API IPS não retorna uma resposta para esta operação.

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
