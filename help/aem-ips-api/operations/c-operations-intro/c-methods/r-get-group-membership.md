---
description: Retorna os membros de um grupo.
seo-description: Retorna os membros de um grupo.
seo-title: getGroupMembship
solution: Experience Manager
title: getGroupMembship
topic: Dynamic Media Image Production System API
uuid: 5ec48e8c-378b-43a3-b3dc-aa21dbf339b5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---


# getGroupMember{#getgroupmembership}

Retorna os membros de um grupo.

Sintaxe

## Tipos de usuário autorizados {#section-35d070e5c4d74ca69df508368953cfb8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-2e92f850254e46e48403acaa215341a5}

**Entrada (getGroupMembationParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Não | O identificador para o usuário. |
| `*`companyHandle`*` | `xsd:string` | Não | A alça da empresa. |

**Saída (getGroupMemberReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`groupArray`*` | `types:GroupArray` | Sim | Matriz de grupos. |

## Exemplos {#section-ebb437369f4f4487b3eb2ef0c078b8ae}

Essa amostra de código retorna todos os membros de um grupo. Como as alças de empresa e usuário são opcionais, a operação pode retornar todos os membros de todos os grupos.

**Solicitação**

```java
<ns1:getGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupMembershipParam>
```

**Resposta**

```java
<getGroupMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle><companyHandle>47</companyHandle><name>MyGroup</name><isSystemDefined>false</isSystemDefined></items></groupArray></getGroupMembershipReturn>
```

