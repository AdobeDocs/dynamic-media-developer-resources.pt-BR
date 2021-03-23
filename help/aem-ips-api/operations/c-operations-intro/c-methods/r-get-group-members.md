---
description: Obtém os usuários que pertencem a uma empresa e grupo específico.
seo-description: Obtém os usuários que pertencem a uma empresa e grupo específico.
seo-title: getGroupMembers
solution: Experience Manager
title: getGroupMembers
uuid: 02322b66-1c0c-4d84-a3eb-97a4fb605318
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '100'
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

