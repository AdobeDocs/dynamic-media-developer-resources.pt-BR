---
description: Define a associação do grupo para um usuário.
solution: Experience Manager
title: setGroupMembership
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 0a355a34-1c2d-48c1-ba12-7d07d1673d09
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# setGroupMembership{#setgroupmembership}

Define a associação do grupo para um usuário.

Sintaxe

## Tipos de usuário autorizados {#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-6aeda13b26af4796aad1306ac7a9ad17}

**Entrada (setGroupMembershipParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Não | O identificador do usuário cuja associação de grupo você deseja definir. |
| `*`companyHandle`*` | `xsd:string` | Não | Manuseio da empresa. |
| `*`groupHandleArray`*` | `types:HandleArray` | Sim | A matriz de grupos aos quais o usuário pertence. |

**Saída (setGroupMembershipReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-67b86d259df24938896fe19061845811}

Essa amostra de código torna o usuário membro de um grupo. Adicione um usuário a vários grupos com a matriz de manipuladores de grupo.

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
