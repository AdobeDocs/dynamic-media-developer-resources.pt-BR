---
description: Remove usuários da empresa de um grupo específico.
solution: Experience Manager
title: removeGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8a9b7d54-d11b-41a8-9783-573a316e0ac6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---

# removeGroupMembers{#removegroupmembers}

Remove usuários da empresa de um grupo específico.

**Diferenças Entre Comandos Remove**

* `removeGroupMembers`: remove vários usuários de um grupo.
* `removeGroupMembership`: remove um usuário individual de uma matriz de grupos.

## Tipos de usuário autorizados {#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-b5596614a3be4ce5962455884e4636af}

**Entrada (removeGroupMembersParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | O identificador da empresa com os usuários com os quais você deseja trabalhar. |
| groupHandle | `xsd:string` | Sim | Identificador de grupo. |
| userHandleArray | `types:HandleArray` | Sim | Uma matriz de identificadores para usuários cujas associações de grupo você deseja remover. |

**Saída (removeGroupMembersParam)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-9eedac852cea46ec80de6a6928bf97ac}

Esta amostra de código remove um usuário da empresa especificada. Remova vários usuários de um grupo com a matriz de identificadores de usuários.

**Solicitação**

```java
<ns1:removeGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>621|jduvar@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:removeGroupMembersParam>
```

**Resposta**

Nenhum.
