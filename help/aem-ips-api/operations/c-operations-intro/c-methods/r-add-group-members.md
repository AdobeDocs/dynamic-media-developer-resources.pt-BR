---
description: Adiciona usuários de uma empresa específica a um grupo específico.
solution: Experience Manager
title: addGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c03525e3-6bc4-4c6a-bb5b-b0cb2e6f6d0d
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# addGroupMembers{#addgroupmembers}

Adiciona usuários de uma empresa específica a um grupo específico.

Sintaxe

## Tipos de usuário autorizados {#section-b4406c54ed7c4827be4c1acc957e0057}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-b28434dcf2ca4b4ea431136aac33913e}

**Entrada (addGroupMembersParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | O identificador da empresa. |
| groupHandle | `xsd:string` | Sim | O identificador do grupo. |
| userHandleArray | `types:HandleArray` | Sim | Uma matriz de identificadores para usuários que você deseja adicionar a um grupo. |

**Saída (addGroupMembersParam)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-8f168b528aef4c4fa8c3d41f7686842f}

Este exemplo usa addGroupMembersParam para adicionar um usuário a uma única empresa. A API do IPS não retorna uma resposta para esta operação.

**Solicitação**

```java {.line-numbers}
<ns1:addGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
<ns1:userHandleArray><ns1:items>70|kmagnusson@adobe.com</ns1:items></ns1:userHandleArray>
</ns1:addGroupMembersParam>
```

**Resposta**

Nenhum.
