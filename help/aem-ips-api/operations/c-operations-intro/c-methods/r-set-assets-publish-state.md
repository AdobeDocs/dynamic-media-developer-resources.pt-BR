---
description: Determina se um lote de ativos está pronto para ser publicado.
solution: Experience Manager
title: setAssetsPublishState
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: dce324e4-cf86-4a65-ab00-8cd2bba20f8f
TQID: 'https://experienceleague.adobe.com/VV11khRodimEOAdPB-6mHR-gIT4AMiKOKeuuH6J15VA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 0%

---

# setAssetsPublishState{#setassetspublishstate}

Determina se um lote de ativos está pronto para ser publicado.

Esta é a versão em lote de [setAssetState](../../../operations/c-operations-intro/c-methods/r-set-asset-publish-state.md#reference-9efc2eeea42348e0b1d5f3d1005c6563).

## Tipos de usuário autorizados {#section-0804726f683944dbbe9acfc3d35ccf25}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>O usuário deve ter acesso de leitura e gravação ao ativo.

## Parâmetros {#section-3e49d7859f8647b990d75373cc8dbc24}

**Entrada (setAssetsPublishStateParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | Identificador da empresa. |
| publishStateUpdateArray | `types:PublishStateUpdateArray` | Sim | Matriz de valores de estado de publicação para os ativos. |

**Saída (setAssetsPublishStateParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| successCount | `xsd:int` | Sim | O número de ativos atualizados com sucesso. |
| warningCount | `xsd:int` | Sim | O número de ativos que geraram um aviso quando a operação tentou atualizá-los. |
| errorCount | `xsd:int` | Sim | O número de ativos que geraram um erro quando a operação tentou excluí-los. |
| warningDetailArray | `types:AssetOperationFaultArray` | Não | Detalhes associados às atualizações de ativos que geraram um aviso. |
| errorDetailArray | `types:AssetOperationFaultArray` | Não | Detalhes associados às atualizações de ativos que geraram um erro. |

## Exemplos {#section-38cfdd3436214a06a1bae16875501d51}

Essa amostra de código define o estado de publicação de um ativo.

**Solicitação**

```java
<element name="setAssetsPublishStateParam">
   <complexType>
      <sequence>
         <element name="companyHandle" type="xsd:string"/>
         <element name="publishStateUpdateArray" type="types:PublishStateUpdateArray"/>
      </sequence>
   </complexType>
</element>
```

**Resposta**

```java
<element name="setAssetsPublishStateReturn">
   <complexType>
      <sequence>
         <element name="successCount" type="xsd:int"/>
         <element name="warningCount" type="xsd:int"/>
         <element name="errorCount" type="xsd:int"/>
         <element name="warningDetailArray"type="types:AssetOperationFaultArray" minOccurs="0"/>
         <element name="errorDetailArray"type="types:AssetOperationFaultArray" minOccurs="0"/>
      </sequence>
   </complexType>
</element>
```

