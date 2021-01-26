---
description: Remove usuários de uma matriz de grupos.
seo-description: Remove usuários de uma matriz de grupos.
seo-title: removeGroupMember
solution: Experience Manager
title: removeGroupMember
topic: Dynamic Media Image Production System API
uuid: 553d91a3-73d6-4323-9436-a3ba13260a6c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---


# removeGroupMember{#removegroupmembership}

Remove usuários de uma matriz de grupos.

**Diferenças entre comandos Remover**

* `removeGroupMembers`: Remove vários usuários de um grupo.
* `removeGroupMembership`: Remove um usuário individual de uma matriz de grupos.

## Tipos de usuário autorizados {#section-83f3048bbe5a4f62b7b14dc9efdd951a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-d6a15fa70d3d4fc69da200cdaf59904e}

**Entrada (removeGroupMembationParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Não | O identificador da empresa cuja associação de grupo você deseja remover. |
| `*`groupHandleArray`*` | `types:HandleArray` | Sim | A matriz de identificadores para grupos dos quais você deseja que a empresa seja removida. |

**Saída (removeGroupMemberReturn)**

A API IPS não retorna uma resposta para esta operação.

## Exemplos {#section-f8d4181170a243efb9faf5824ae96197}

Esta amostra de código remove um usuário de um grupo.

**Solicitação**

```java
<ns1:removeGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>47</ns1:userHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:removeGroupMembershipParam>
```

**Resposta**

Nenhum.
