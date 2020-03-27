---
description: Cria um novo ativo derivado de um ativo de imagem mestre existente.
seo-description: Cria um novo ativo derivado de um ativo de imagem mestre existente.
seo-title: createDeriveAsset
solution: Experience Manager
title: createDeriveAsset
topic: Scene7 Image Production System API
uuid: e1f9b690-af34-4da5-a534-c3a8c6b0a8fc
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# createDeriveAsset{#createderivedasset}

Cria um novo ativo derivado de um ativo de imagem mestre existente.

Sintaxe

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

Os ativos derivados especificam comandos de protocolo do Servidor de imagens que modificam a representação da imagem do proprietário. O tipo `AdjustedView` derivado ajuda a aplicar modificações simples em uma única imagem (por exemplo, especificando um retângulo de corte), enquanto o `LayerView` ajuda a criar uma visualização de várias camadas que pode incluir texto ou imagens adicionais.

Ao contrário de uma cópia de imagem (consulte [copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0)), uma imagem derivada é vinculada à imagem proprietária. As alterações na imagem do proprietário modificam os ativos derivados associados. A exclusão da imagem proprietária excluirá qualquer imagem derivada associada.

## Tipos de usuário autorizados {#authorized-user-types}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-5a0dde01cff6454da3646ea805c2be1e}

**Entrada (createDeriveAssetParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa que contém o ativo do qual você derivará o novo ativo. |
| ` *`ownerHandle`*` | `xsd:string` | Sim | O identificador do ativo de imagem mestre a partir do qual a nova imagem será derivada. |
| ` *`folderHandle`*` | `xsd:string` | Sim | O identificador da pasta na qual o novo ativo derivado será criado. |
| ` *`name`*` | `xsd:string` | Sim | O nome do ativo derivado. |
| ` *`type`*` | `xsd:string` | Sim | O tipo de ativo do novo ativo derivado: `AdjustedView` ou `LayerView`. |
| ` *`urlModifier`*` | `xsd:string` | Não | Comandos do protocolo de disponibilização de imagem ou renderização de imagem aplicados *antes* da solicitação ou dos `urlPostApplyModifier` comandos. |
| ` *`urlPostApplyModifier`*` | `xsd:string` | Não | Comandos do protocolo de disponibilização de imagem ou renderização de imagem aplicados *após* a solicitação ou os `urlPostApplyModifier` comandos. |

**Saída (createDerivingAssetParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Sim | O identificador do ativo derivado. |

## Exemplos {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

O código de amostra cria um ativo derivado com uma visualização ajustada `urlModifier` e `urlPostApplyModifier` com valores arbitrários. A resposta retorna o identificador para o ativo recém-derivado.

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

