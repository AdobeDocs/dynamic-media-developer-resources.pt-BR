---
description: Obtém projetos para um grupo de ativos relacionados.
seo-description: Obtém projetos para um grupo de ativos relacionados.
seo-title: getProjects
solution: Experience Manager
title: getProjects
uuid: 46ec9a5d-4414-4c9c-aaf2-0db654204b61
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '82'
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
| `*`companyHandle`*` | `xsd:string` | Sim | O nome da empresa. |

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

