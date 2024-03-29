---
description: Obtém os usuários que pertencem a uma empresa e a um grupo específicos.
solution: Experience Manager
title: getGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81af79ee-be82-439f-9f42-a1ec09cd8ea0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# getGroupMembers{#getgroupmembers}

Obtém os usuários que pertencem a uma empresa e a um grupo específicos.

Sintaxe

## Tipos de usuário autorizados {#section-08a73460d122480292205bb8f2df9220}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-b798b06354c946abbb90fa72cc9c67fd}

**Entrada (getGroupMembersParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | O identificador da empresa. |
| groupHandle | `xsd:string` |  | O identificador do grupo. |

**Saída (getGroupMembersReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| userHandleArray | `type:HandleArray` | Sim | Uma matriz de manipuladores de usuário. |

## Exemplos {#section-aaa340dba6b64cce9bcd8303cf999166}

Essa amostra de código retorna uma matriz de identificadores de usuário que contém todos os usuários que pertencem a um grupo específico.

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
