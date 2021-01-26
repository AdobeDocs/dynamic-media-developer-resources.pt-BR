---
description: Obtém projetos para um grupo de ativos relacionados.
seo-description: Obtém projetos para um grupo de ativos relacionados.
seo-title: getProjects
solution: Experience Manager
title: getProjects
topic: Dynamic Media Image Production System API
uuid: 46ec9a5d-4414-4c9c-aaf2-0db654204b61
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---


# getProjects{#getprojects}

Obtém projetos para um grupo de ativos relacionados.

Sintaxe

## Tipos de usuário autorizados {#section-337649866b1f4098844d1974ed7ab5d0}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-8d549237b8c440b4872a0a086ddc00a1}

**Entrada (getProjectsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | A alça da empresa. |

**Saída (getProjectsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`projectArray`*` | `types:ProjectArray` | Sim | A matriz de projetos associados à empresa. |

## Exemplos {#section-8b12d0b948f644f68bf9a16060d3849a}

Esta amostra de código retorna todos os identificadores de projeto em uma matriz de projeto.

**Solicitação**

```java
<ns1:getProjectsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getProjectsParam>
```

**Resposta**

```java
<getProjectsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <projectArray>
      <items>
         <projectHandle>47|My Project 1</projectHandle>
         <name>My Project 1</name>
      </items>
      <items>
         <projectHandle>47|My Project 2</projectHandle>
         <name>My Project 2</name>
      </items>
   </projectArray>
</getProjectsReturn>
```

