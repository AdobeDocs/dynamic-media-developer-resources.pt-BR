---
description: Adiciona usuários de uma empresa específica a um grupo específico.
solution: Experience Manager
title: addGroupMembers
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---


# addGroupMembers{#addgroupmembers}

Adiciona usuários de uma empresa específica a um grupo específico.

Sintaxe

## Tipos de usuário autorizados {#section-b4406c54ed7c4827be4c1acc957e0057}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-b28434dcf2ca4b4ea431136aac33913e}

**Entrada (addGroupMembersParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O nome da empresa. |
| `*`groupHandle`*` | `xsd:string` | Sim | O identificador de grupo. |
| `*`userHandleArray`*` | `types:HandleArray` | Sim | Uma matriz de usuários que você deseja adicionar a um grupo. |

**Saída (addGroupMembersParam)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-8f168b528aef4c4fa8c3d41f7686842f}

Este exemplo usa `*`addGroupMembersParam`*` para adicionar um usuário a uma única empresa. A API do IPS não retorna uma resposta para esta operação.

**Solicitação**

```java
<ns1:addGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
<ns1:userHandleArray><ns1:items>70|kmagnusson@adobe.com</ns1:items></ns1:userHandleArray>
</ns1:addGroupMembersParam>
```

**Resposta**

Nenhum.
