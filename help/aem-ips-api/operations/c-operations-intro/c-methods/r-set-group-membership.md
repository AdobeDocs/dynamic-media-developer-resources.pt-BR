---
description: Define a associação de grupo de um usuário.
solution: Experience Manager
title: setGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0a355a34-1c2d-48c1-ba12-7d07d1673d09
TQID: 'https://experienceleague.adobe.com/j-wK2g-evSRY0YD3ZspgT--giCkKJl1VBYgPylixVz8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 96
ht-degree: 0%

---

# setGroupMembership{#setgroupmembership}

Define a associação de grupo de um usuário.

Sintaxe

## Tipos de usuário autorizados {#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-6aeda13b26af4796aad1306ac7a9ad17}

**Entrada (setGroupMembershipParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| userHandle | `xsd:string` | Não | O identificador do usuário cuja associação de grupo você deseja definir. |
| companyHandle | `xsd:string` | Não | Identificador da empresa. |
| groupHandleArray | `types:HandleArray` | Sim | A matriz de identificadores a grupos aos quais o usuário pertence. |

**Saída (setGroupMembershipReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-67b86d259df24938896fe19061845811}

Essa amostra de código torna o usuário membro de um grupo. Adicione um usuário a vários grupos com a matriz de identificadores de grupo.

**Solicitação**

```java
<ns1:setGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:setGroupMembershipParam>
```

**Resposta**

Nenhum.

