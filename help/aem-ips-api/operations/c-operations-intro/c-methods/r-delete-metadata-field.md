---
description: Exclui um campo de metadados da empresa.
solution: Experience Manager
title: deleteMetadataField
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1922fc1b-2abc-4d31-985a-65c788af4d46
TQID: 'https://experienceleague.adobe.com/GnKkb-vTCdD5PwU111sxefzxR7FN74hk3i66c3gcH9I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 99
ht-degree: 0%

---

# deleteMetadataField{#deletemetadatafield}

Exclui um campo de metadados da empresa.

Sintaxe

## Tipos de usuário autorizados {#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-73f12a30cc4340b6b32dd11effd5195e}

**Entrada (deleteMetadataFieldParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | O identificador da empresa que contém o campo de metadados a ser excluído. |
| fieldHandle | `xsd:string` | Sim | O identificador para o campo de metadados a ser excluído. |

**Saída (deleteMetadataFieldParam)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-e1c474ea91a040609ecd7c2400f4fa3c}

Essa amostra de código exclui o campo de metadados de uma empresa. Ele usa o identificador da empresa e o identificador de metadados como campos no `deleteMetadataFieldParam` passado para o servidor de serviços Web IPS para executar esta ação.

**Solicitação**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**Resposta**

Nenhum.0
