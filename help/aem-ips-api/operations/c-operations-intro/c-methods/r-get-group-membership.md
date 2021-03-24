---
description: Retorna os membros de um grupo.
solution: Experience Manager
title: getGroupMembership
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---


# getGroupMembership{#getgroupmembership}

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

**Entrada (getGroupMembershipParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Não | O identificador para o usuário. |
| `*`companyHandle`*` | `xsd:string` | Não | O nome da empresa. |

**Saída (getGroupMembershipReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`groupArray`*` | `types:GroupArray` | Sim | Matriz de grupos. |

## Exemplos {#section-ebb437369f4f4487b3eb2ef0c078b8ae}

Essa amostra de código retorna todos os membros de um grupo. Como os identificadores de empresa e usuário são opcionais, a operação pode retornar todos os membros de todos os grupos.

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

