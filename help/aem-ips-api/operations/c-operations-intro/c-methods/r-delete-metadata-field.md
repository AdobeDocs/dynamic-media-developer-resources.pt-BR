---
description: Exclui o campo de metadados de uma empresa.
seo-description: Exclui o campo de metadados de uma empresa.
seo-title: deleteMetadataField
solution: Experience Manager
title: deleteMetadataField
uuid: 06ec434a-2793-4227-ac93-ae3871c38ab9
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---


# deleteMetadataField{#deletemetadatafield}

Exclui o campo de metadados de uma empresa.

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
| `*`fieldHandle`*` | `xsd:string` | Sim | O identificador do campo de metadados que será excluído. |

**Saída (deleteMetadataFieldParam)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-e1c474ea91a040609ecd7c2400f4fa3c}

Essa amostra de código exclui o campo de metadados de uma empresa. Ele usa o identificador da empresa e o identificador de metadados como campos no `deleteMetadataFieldParam` passado para o servidor de serviços Web IPS para executar essa ação.

**Solicitação**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**Resposta**

Nenhum.0
