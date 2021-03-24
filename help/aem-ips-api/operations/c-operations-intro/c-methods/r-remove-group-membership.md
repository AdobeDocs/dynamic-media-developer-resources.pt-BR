---
description: Remove usuários de uma matriz de grupos.
solution: Experience Manager
title: removeGroupMembership
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# removeGroupMembership{#removegroupmembership}

Remove usuários de uma matriz de grupos.

**Diferenças entre comandos Remover**

* `removeGroupMembers`: Remove vários usuários de um grupo.
* `removeGroupMembership`: Remove um usuário individual de uma matriz de grupos.

## Tipos de usuário autorizados {#section-83f3048bbe5a4f62b7b14dc9efdd951a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-d6a15fa70d3d4fc69da200cdaf59904e}

**Entrada (removeGroupMembershipParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Não | O identificador da empresa cuja associação de grupo você deseja remover. |
| `*`groupHandleArray`*` | `types:HandleArray` | Sim | A matriz de grupos a partir dos quais você deseja que a empresa seja removida. |

**Saída (removeGroupMembershipReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-f8d4181170a243efb9faf5824ae96197}

Essa amostra de código remove um usuário de um grupo.

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
