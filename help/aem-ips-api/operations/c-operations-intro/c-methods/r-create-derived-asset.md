---
description: Cria um novo ativo derivado de um ativo de imagem de origem primária existente.
seo-description: Cria um novo ativo derivado de um ativo de imagem de origem primária existente.
seo-title: createDerivedAsset
solution: Experience Manager
title: createDerivedAsset
uuid: e1f9b690-af34-4da5-a534-c3a8c6b0a8fc
feature: Dynamic Media Classic, SDK/API, Gerenciamento de ativos
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---


# createDerivedAsset{#createderivedasset}

Cria um novo ativo derivado de um ativo de imagem de origem primária existente.

Sintaxe

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

Os ativos derivados especificam comandos de protocolo do Servidor de Imagem que modificam a representação da imagem do proprietário. O tipo derivado `AdjustedView` ajuda a aplicar modificações simples a uma única imagem (por exemplo, ao especificar um retângulo de corte), enquanto o `LayerView` ajuda a criar uma visualização com várias camadas que pode incluir texto ou imagens adicionais.

Ao contrário de uma cópia de imagem (consulte [copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0)), uma imagem derivada é vinculada à imagem proprietária. Alterações na imagem do proprietário modifica ativos derivados associados. A exclusão da imagem do proprietário excluirá quaisquer imagens derivadas associadas.

## Tipos de usuário autorizados {#authorized-user-types}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-5a0dde01cff6454da3646ea805c2be1e}

**Entrada (createDerivedAssetParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador para a empresa que contém o ativo do qual você vai derivar o novo ativo. |
| `*`ownerHandle`*` | `xsd:string` | Sim | O identificador para o ativo principal de Imagem do qual a nova imagem será derivada. |
| `*`folderHandle`*` | `xsd:string` | Sim | O identificador da pasta na qual o novo ativo derivado será criado. |
| `*`name`*` | `xsd:string` | Sim | O nome do ativo derivado. |
| `*`type`*` | `xsd:string` | Sim | O tipo de ativo do novo ativo derivado: `AdjustedView` ou `LayerView`. |
| `*`urlModifier`*` | `xsd:string` | Não | Os comandos do protocolo Image Serving ou image rendering eram aplicados *antes de* da solicitação ou dos comandos `urlPostApplyModifier`. |
| `*`urlPostApplyModifier`*` | `xsd:string` | Não | Comandos de protocolo de disponibilização de imagens ou renderização de imagens aplicados *after* aos comandos request ou `urlPostApplyModifier`. |

**Saída (createDerivedAssetParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Sim | O identificador do ativo derivado. |

## Exemplos {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

O código de amostra cria um ativo derivado com uma exibição ajustada e `urlModifier` e `urlPostApplyModifier` com valores arbitrários. A resposta retorna o identificador para o ativo recém-derivado.

**Solicitação**

```java
<createDerivedAssetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <ownerHandle>a|943|1|580</ownerHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>ApiDerivedAsset</name>
   <type>AdjustedView</type>
   <urlModifier>modify=this</urlModifier>
   <urlPostApplyModifier>action=awesome</urlPostApplyModifier>
</createDerivedAssetParam>
```

**Resposta**

```java
<createDerivedAssetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|944|10|2</assetHandle>
</createDerivedAssetReturn>
```

