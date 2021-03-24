---
description: Define a associação de grupo de usuários que pertencem a uma empresa específica.
solution: Experience Manager
title: setGroupMembers
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---


# setGroupMembers{#setgroupmembers}

Define a associação de grupo de usuários que pertencem a uma empresa específica.

A operação gera uma falha de autenticação se você não tiver privilégios para realizar essa operação. Isso também é verdade se qualquer um dos usuários na matriz de identificador do usuário não pertencer à empresa especificada no identificador da empresa,

## Tipos de usuário autorizados {#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-6a18562fc8e942af94be10bbb8c51151}

**Entrada (setGroupMembersParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | Manuseio da empresa. |
| `*`groupHandle`*` | `xsd:string` | Sim | Identificador de grupo. |
| `*`userHandleArray`*` | `types:HandleArray` | Sim | Matriz de identificadores para usuários cuja associação de grupo você deseja definir. |

**Saída (setGroupMembesReturn)**

A API do IPS não retorna uma resposta para esta operação.

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
