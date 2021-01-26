---
description: Retorna grupos de empresas.
seo-description: Retorna grupos de empresas.
seo-title: getGroups
solution: Experience Manager
title: getGroups
topic: Dynamic Media Image Production System API
uuid: d6e1542d-83a2-4b25-a986-2465e9e5a145
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '65'
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
| `*`companyHandle`*` | `xsd:string` | Sim | A alça da empresa. |

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

