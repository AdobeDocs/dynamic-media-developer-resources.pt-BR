---
description: Retorna grupos de empresas.
solution: Experience Manager
title: getGroups
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: d98c08a6-4c20-4538-9598-c905078ab7de
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 0%

---

# getGroups{#getgroups}

Retorna grupos de empresas.

Sintaxe

## Tipos de usuário autorizados {#section-27c77680a2f34e2f9ecd0af4ebb6847e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-0e06195f23dd4c69922df210f566dd18}

**Entrada (getGroupsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O nome da empresa. |

**Saída (getGroupsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`groupArray`*` | `types:GroupArray` | Sim | Matriz de grupos. |

## Exemplos {#section-ed0708f611574354bf0c6ea83912b531}

Esse código retorna uma matriz que contém todos os grupos que pertencem a uma empresa específica e informações específicas sobre cada grupo.

**Solicitação**

```java
<ns1:getGroupsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupsParam>
```

```java
<getGroupsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle>
         <companyHandle>47</companyHandle>
         <name>MyGroup</name>
         <isSystemDefined>false</isSystemDefined>
      </items>
   </groupArray>
</getGroupsReturn>
```
