---
description: Remove usuários de uma matriz de grupos.
seo-description: Remove usuários de uma matriz de grupos.
seo-title: removeGroupMembership
solution: Experience Manager
title: removeGroupMembership
uuid: 553d91a3-73d6-4323-9436-a3ba13260a6c
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '117'
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
