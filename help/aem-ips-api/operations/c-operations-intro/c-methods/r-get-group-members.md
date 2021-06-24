---
description: Obtém os usuários que pertencem a uma empresa e grupo específico.
solution: Experience Manager
title: getGroupMembers
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 81af79ee-be82-439f-9f42-a1ec09cd8ea0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# getGroupMembers{#getgroupmembers}

Obtém os usuários que pertencem a uma empresa e grupo específico.

Sintaxe

## Tipos de usuário autorizados {#section-08a73460d122480292205bb8f2df9220}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-b798b06354c946abbb90fa72cc9c67fd}

**Entrada (getGroupMembersParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O nome da empresa. |
| `*`groupHandle`*` | `xsd:string` |  | O identificador do grupo. |

**Saída (getGroupMembersReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`userHandleArray`*` | `type:HandleArray` | Sim | Uma matriz de identificadores de usuários. |

## Exemplos {#section-aaa340dba6b64cce9bcd8303cf999166}

Essa amostra de código retorna uma matriz de identificador do usuário contendo todos os usuários que pertencem a um grupo específico.

**Solicitação**

```java
<ns1:getGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
</ns1:getGroupMembersParam>
```

**Resposta**

```java
<getGroupMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userHandleArray>
      <items>70|kmagnusson@adobe.com</items>
   </userHandleArray>
</getGroupMembersReturn>
```
