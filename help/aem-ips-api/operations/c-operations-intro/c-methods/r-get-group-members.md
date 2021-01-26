---
description: Obtém os usuários que pertencem a uma empresa e grupo específicos.
seo-description: Obtém os usuários que pertencem a uma empresa e grupo específicos.
seo-title: getGroupMembers
solution: Experience Manager
title: getGroupMembers
topic: Dynamic Media Image Production System API
uuid: 02322b66-1c0c-4d84-a3eb-97a4fb605318
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# getGroupMembers{#getgroupmembers}

Obtém os usuários que pertencem a uma empresa e grupo específicos.

Sintaxe

## Tipos de usuário autorizados {#section-08a73460d122480292205bb8f2df9220}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-b798b06354c946abbb90fa72cc9c67fd}

**Entrada (getGroupMembersParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | A alça da empresa. |
| `*`groupHandle`*` | `xsd:string` |  | O identificador do grupo. |

**Saída (getGroupMembersReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`userHandleArray`*` | `type:HandleArray` | Sim | Uma matriz de identificadores de usuário. |

## Exemplos {#section-aaa340dba6b64cce9bcd8303cf999166}

Esta amostra de código retorna uma matriz de identificador de usuário contendo todos os usuários que pertencem a um grupo específico.

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

