---
description: Determina se um lote de ativos está pronto para ser publicado.
seo-description: Determina se um lote de ativos está pronto para ser publicado.
seo-title: setAssetsPublishState
solution: Experience Manager
title: setAssetsPublishState
uuid: 2910cd6c-573b-405c-864d-a0136ac5472d
feature: Dynamic Media Classic, SDK/API, Gerenciamento de ativos
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '172'
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
| `*`companyHandle`*` | `xsd:string` | Sim | Manuseio da empresa. |
| `*`publishStateUpdateArray`*` | `types:PublishStateUpdateArray` | Sim | Matriz de valores de estado de publicação para os ativos. |

**Saída (setAssetsPublishStateParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sim | A quantidade de ativos atualizados com êxito. |
| `*`warningCount`*` | `xsd:int` | Sim | O número de ativos que geraram um aviso quando a operação tentou atualizá-los. |
| `*`errorCount`*` | `xsd:int` | Sim | O número de ativos que geraram um erro quando a operação tentou excluí-los. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Não | Detalhes associados às atualizações de ativos que geraram um aviso. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Não | Detalhes associados às atualizações de ativos que geraram um erro. |

## Exemplos {#section-38cfdd3436214a06a1bae16875501d51}

Essa amostra de código define o estado da publicação de um ativo.

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

