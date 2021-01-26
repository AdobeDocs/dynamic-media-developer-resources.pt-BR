---
description: Renomeia um ativo.
seo-description: Renomeia um ativo.
seo-title: renameAsset
solution: Experience Manager
title: renameAsset
topic: Dynamic Media Image Production System API
uuid: f285d7e4-00df-4d90-a05a-71747a4c54cc
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---


# renameAsset{#renameasset}

Renomeia um ativo.

>[!NOTE]
>
>O parâmetro `renameFiles` foi preterido para versões anteriores e removido de `renameAsset`. O caminho do arquivo virtual é alterado para corresponder ao novo nome do ativo (preservando a extensão do arquivo), enquanto os caminhos do arquivo físico não são afetados. Os clientes da API precisam remover referências a esse parâmetro ao atualizar para a nova versão da API.

## Tipos de usuário autorizados {#section-cc27ad713c6d498b8f056850b20976f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImpagePortalContribUser`

>[!NOTE]
>
>O usuário deve ter acesso de leitura e gravação ao ativo.

## Parâmetros {#section-ef95a994106841e0ab346dd4cf672258}

**Entrada (renameAssetParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa à qual o ativo pertence. |
| `*`assetHandle`*` | `xsd:string` | Sim | O identificador do ativo que você deseja renomear. |
| `*`newName`*` | `xsd:string` | Sim | O novo nome do ativo. |
| `*`validateName`*` | `xsd:boolean` | Sim | Se `validateName` for `true` e o tipo de ativo exigir uma ID IPS exclusiva, o novo nome será verificado quanto à exclusividade global e `renameAsset` emitirá uma falha se não for exclusiva. |

**Saída (renameAssetReturn)**

A API IPS não retorna uma resposta para esta operação. Consulte a descrição do elemento `<ns1:validateName>` para obter avisos sobre esse elemento.

## Exemplos {#section-a0ddffd62bec42e09069f22ceb486f8a}

Essa amostra de código renomeia um ativo

**Solicitação**

```java
<ns1:renameAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:newName>My Newly Renamed Image</ns1:newName>
   <ns1:validateName>true</ns1:validateName>
   <ns1:renameFiles>true</ns1:renameFiles>
</ns1:renameAssetParam>
```

**Resposta**

Nenhum.
