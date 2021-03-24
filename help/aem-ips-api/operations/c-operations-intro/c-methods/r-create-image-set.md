---
description: Cria um conjunto de imagens.
solution: Experience Manager
title: createImageSet
feature: Dynamic Media Classic, SDK/API, Conjuntos de imagens
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# createImageSet{#createimageset}

Cria um conjunto de imagens.

Sintaxe

## Tipos de usuário autorizados {#section-58bf5027e6d24ab5a9fcba59776d15dc}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>O usuário deve ter acesso de leitura/gravação à pasta de destino.

## Parâmetros {#section-03d22ba7d290477e91c25ca1d4439200}

**Entrada (createImageSetParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa à qual o conjunto de imagens pertence. |
| `*`folderHandle`*` | `xsd:string` | Sim | O identificador da pasta. |
| `*`name`*` | `xsd:string` | Sim | Nome do conjunto de imagens. |
| `*`type`*` | `xsd:string` | Sim | Tipo de conjunto de imagens. |
| `*`thumbAssetHandle`*` | `xsd:string` | Não | Gerenciar o ativo que atua como a miniatura do novo conjunto de imagens. Se não especificado, o IPS tentará usar o primeiro ativo de imagem referenciado pelo conjunto. |

**Saída**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Sim | O identificador do novo conjunto de imagens. |

## Exemplos {#section-385fe3b0af8044b0a2451336ec137fc5}

Essa amostra de código cria um conjunto de imagens especificado por empresa, pasta, nome e tipo. A resposta é um identificador de ativo do conjunto de imagens recém-criado.

**Solicitação**

```java
<ns1:createImageSetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/eCatalogs/</ns1:folderHandle>
   <ns1:name>My Image Set</ns1:name>
   <ns1:type>ImageSet</ns1:type>
</ns1:createImageSetParam>
```

**Resposta**

```java
<createImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <assetHandle>25741|22|841</assetHandle>
</createImageSetReturn>
```

