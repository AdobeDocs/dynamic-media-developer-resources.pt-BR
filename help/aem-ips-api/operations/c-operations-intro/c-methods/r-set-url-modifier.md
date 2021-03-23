---
description: Define os comandos do protocolo Image Serving ou Image Rendering para o ativo especificado. Esses comandos modificam a representação do ativo sem destruí-lo.
seo-description: Define os comandos do protocolo Image Serving ou Image Rendering para o ativo especificado. Esses comandos modificam a representação do ativo sem destruí-lo.
seo-title: setUrlModifier
solution: Experience Manager
title: setUrlModifier
uuid: ec423e57-338b-4a32-be5a-a73fa96712ce
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---


# setUrlModifier{#seturlmodifier}

Define os comandos do protocolo Image Serving ou Image Rendering para o ativo especificado. Esses comandos modificam a representação do ativo sem destruí-lo.

Para o Image Serving, os comandos no parâmetro `urlModifier` são publicados no campo Modificador do catálogo e aplicados antes de qualquer comando especificado no URL da solicitação. Os comandos em `urlPostApplyModifier` serão publicados no campo de catálogo `PostModifier` e substituirão quaisquer comandos no URL da solicitação ou em `urlModifier`. Para Renderização de imagem, os comandos em `urlModifier` e `urlPostApplyModifier` são concatenados e publicados no campo de catálogo Modificador.

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
| `*`companyHandle`*` | `xsd:string` | Sim | Manuseio da empresa. |
| `*`assetHandle`*` | `xsd:string` | Sim | Identificador de ativo. |
| `*`urlModifier`*` | `xsd:string` | Não | Comandos do protocolo Image Serving ou Image Rendering para aplicar antes dos comandos request ou `urlPostApplyModifier` . |
| `*`urlPostApplyModifier`*` | `xsd:string` | Não | Comandos do protocolo Image Serving ou Image Rendering para aplicar depois de `urlModifier` e solicitar comandos. |

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
