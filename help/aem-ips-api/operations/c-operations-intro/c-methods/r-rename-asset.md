---
description: Renomeia um ativo.
solution: Experience Manager
title: renameAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f3fff3c1-1b48-4d86-8a81-f75be00fc329
TQID: 'https://experienceleague.adobe.com/m1AT0yP7u3PFZCs8uoFQxQoGNtfJe49vzGt8e3wTx8s'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 173
ht-degree: 0%

---

# renameAsset{#renameasset}

Renomeia um ativo.

>[!NOTE]
>
>O parâmetro `renameFiles` foi substituído em versões anteriores e removido de `renameAsset`. O caminho do arquivo virtual é alterado para corresponder ao novo nome do ativo (preservando a extensão do arquivo), enquanto os caminhos do arquivo físico não são afetados. Os clientes da API precisam remover as referências a esse parâmetro ao atualizar para a nova versão da API.

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
| companyHandle | `xsd:string` | Sim | O identificador da empresa à qual o ativo pertence. |
| assetHandle | `xsd:string` | Sim | O identificador do ativo que você deseja renomear. |
| newName | `xsd:string` | Sim | Novo nome do ativo. |
| validateName | `xsd:boolean` | Sim | Se o `validateName` for `true` e o tipo de ativo exigir uma ID de IPS exclusiva, o novo nome será verificado para exclusividade global e `renameAsset` acionará uma falha se não for exclusiva. |

**Saída (renameAssetReturn)**

A API do IPS não retorna uma resposta para esta operação. Consulte a descrição do elemento `<ns1:validateName>` para avisos sobre esse elemento.

## Exemplos {#section-a0ddffd62bec42e09069f22ceb486f8a}

Esta amostra de código renomeia um ativo

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
