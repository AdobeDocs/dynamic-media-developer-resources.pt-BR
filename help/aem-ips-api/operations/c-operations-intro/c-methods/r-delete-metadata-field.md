---
description: Exclui um campo de metadados de empresa.
seo-description: Exclui um campo de metadados de empresa.
seo-title: deleteMetadataField
solution: Experience Manager
title: deleteMetadataField
topic: Dynamic Media Image Production System API
uuid: 06ec434a-2793-4227-ac93-ae3871c38ab9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---


# deleteMetadataField{#deletemetadatafield}

Exclui um campo de metadados de empresa.

Sintaxe

## Tipos de usuário autorizados {#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-73f12a30cc4340b6b32dd11effd5195e}

**Entrada (deleteMetadataFieldParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa que contém o campo de metadados a ser excluído. |
| `*`fieldHandle`*` | `xsd:string` | Sim | O identificador do campo de metadados a ser excluído. |

**Saída (deleteMetadataFieldParam)**

A API IPS não retorna uma resposta para esta operação.

## Exemplos {#section-e1c474ea91a040609ecd7c2400f4fa3c}

Essa amostra de código exclui um campo de metadados de empresa. Ele usa o identificador de empresa e o identificador de metadados como campos no `deleteMetadataFieldParam` passado para o servidor de serviços Web IPS para executar essa ação.

**Solicitação**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**Resposta**

Nenhum.0
