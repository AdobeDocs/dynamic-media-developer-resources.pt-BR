---
description: Remove usuários da empresa de um grupo específico.
solution: Experience Manager
title: removeGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# removeGroupMembers{#removegroupmembers}

Remove usuários da empresa de um grupo específico.

**Diferenças entre comandos Remover**

* `removeGroupMembers`: Remove vários usuários de um grupo.
* `removeGroupMembership`: Remove um usuário individual de uma matriz de grupos.

## Tipos de usuário autorizados {#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-b5596614a3be4ce5962455884e4636af}

**Entrada (removeGroupMembersParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | A conta com a empresa com os usuários com os quais deseja trabalhar. |
| `*`groupHandle`*` | `xsd:string` | Sim | Identificador de grupo. |
| `*`userHandleArray`*` | `types:HandleArray` | Sim | Uma matriz de identificadores para usuários cujas associações de grupo você deseja remover. |

**Saída (removeGroupMembersParam)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-9eedac852cea46ec80de6a6928bf97ac}

Esta amostra de código remove um usuário da empresa especificada. Remova vários usuários de um grupo com a matriz de identificador do usuário.

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
