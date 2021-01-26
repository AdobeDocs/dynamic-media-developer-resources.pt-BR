---
description: Define a associação de grupo de usuários que pertencem a uma empresa específica.
seo-description: Define a associação de grupo de usuários que pertencem a uma empresa específica.
seo-title: setGroupMembers
solution: Experience Manager
title: setGroupMembers
topic: Dynamic Media Image Production System API
uuid: fe6585ef-a4b3-4b3c-95d0-624017650497
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---


# setGroupMembers{#setgroupmembers}

Define a associação de grupo de usuários que pertencem a uma empresa específica.

A operação gera uma falha de autenticação se você não tiver privilégios para realizar essa operação. Isso também é verdadeiro se algum usuário na matriz de identificador do usuário não pertencer à empresa especificada no identificador de empresa,

## Tipos de usuário autorizados {#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-6a18562fc8e942af94be10bbb8c51151}

**Entrada (setGroupMembersParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | Alça da empresa. |
| `*`groupHandle`*` | `xsd:string` | Sim | Identificador de grupo. |
| `*`userHandleArray`*` | `types:HandleArray` | Sim | Matriz de identificadores para usuários cuja associação de grupo você deseja definir. |

**Saída (setGroupMembesReturn)**

A API IPS não retorna uma resposta para esta operação.

## Exemplos {#section-9c528c3f44a141ce9eaddf634f26c487}

Esta amostra de código define a associação de grupo para um único usuário.

**Solicitação**

```java
<ns1:setGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>70|kmagnusson@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:setGroupMembersParam>
```

**Resposta**

Nenhum.
