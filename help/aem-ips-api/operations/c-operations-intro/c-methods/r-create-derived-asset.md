---
description: Cria um novo ativo derivado de um ativo de imagem de origem primária existente.
solution: Experience Manager
title: createDerivedAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: a3b20a8a-ed0d-40be-9a8c-41ba09b1d724
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# createDerivedAsset{#createderivedasset}

Cria um novo ativo derivado de um ativo de imagem de origem primária existente.

Sintaxe

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

Os ativos derivados especificam comandos de protocolo do Servidor de Imagem que modificam a representação da imagem do proprietário. O `AdjustedView` o tipo derivado ajuda a aplicar modificações simples em uma única imagem (por exemplo, ao especificar um retângulo de corte), enquanto o `LayerView` ajuda a criar uma visualização com várias camadas, que pode incluir texto ou imagens adicionais.

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
| companyHandle | `xsd:string` | Sim | O identificador para a empresa que contém o ativo do qual você vai derivar o novo ativo. |
| ownerHandle | `xsd:string` | Sim | O identificador para o ativo de Imagem principal do qual a nova imagem é derivada. |
| folderHandle | `xsd:string` | Sim | O identificador da pasta em que o novo ativo derivado é criado. |
| name | `xsd:string` | Sim | O nome do ativo derivado. |
| type | `xsd:string` | Sim | O tipo de ativo do novo ativo derivado: `AdjustedView` ou `LayerView`. |
| urlModifier | `xsd:string` | Não | Comandos do protocolo de disponibilização de imagens ou de renderização de imagens aplicados *before* o pedido ou `urlPostApplyModifier` comandos. |
| urlPostApplyModifier | `xsd:string` | Não | Comandos do protocolo de disponibilização de imagens ou de renderização de imagens aplicados *after* ao pedido ou `urlPostApplyModifier` comandos. |

**Saída (createDerivedAssetParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| assetHandle | `xsd:string` | Sim | O identificador do ativo derivado. |

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
