---
description: Define os comandos do protocolo Servidor de imagens ou Renderização de imagens para o ativo especificado. Esses comandos modificam a representação do ativo sem destruí-lo.
seo-description: Define os comandos do protocolo Servidor de imagens ou Renderização de imagens para o ativo especificado. Esses comandos modificam a representação do ativo sem destruí-lo.
seo-title: setUrlModifier
solution: Experience Manager
title: setUrlModifier
topic: Scene7 Image Production System API
uuid: ec423e57-338b-4a32-be5a-a73fa96712ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setUrlModifier{#seturlmodifier}

Define os comandos do protocolo Servidor de imagens ou Renderização de imagens para o ativo especificado. Esses comandos modificam a representação do ativo sem destruí-lo.

Para o Serviço de imagem, os comandos no `urlModifier` parâmetro são publicados no campo de catálogo Modificador e aplicados antes de qualquer comando especificado no URL da solicitação. Os comandos em `urlPostApplyModifier` serão publicados no campo de `PostModifier` catálogo e substituirão quaisquer comandos no URL da solicitação ou em `urlModifier`. Para renderização de imagem, os comandos em `urlModifier` e `urlPostApplyModifier` são concatenados e publicados no campo de catálogo Modificador.

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
| ` *`companyHandle`*` | `xsd:string` | Sim | Alça da Empresa. |
| ` *`assetHandle`*` | `xsd:string` | Sim | Identificador de ativos. |
| ` *`urlModifier`*` | `xsd:string` | Não | Comandos do protocolo de disponibilização ou renderização de imagem a serem aplicados antes da solicitação ou `urlPostApplyModifier` dos comandos. |
| ` *`urlPostApplyModifier`*` | `xsd:string` | Não | Comandos do protocolo de disponibilização de imagens ou renderização de imagens para aplicar depois `urlModifier` e solicitar comandos. |

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
