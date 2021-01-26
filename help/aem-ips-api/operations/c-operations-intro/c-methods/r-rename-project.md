---
description: Renomeia um projeto.
seo-description: Renomeia um projeto.
seo-title: renameProject
solution: Experience Manager
title: renameProject
topic: Dynamic Media Image Production System API
uuid: 6303c493-a6fe-4b32-80c3-947aba4190f7
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---


# renameProject{#renameproject}

Renomeia um projeto.

Sintaxe

## Tipos de usuário autorizados {#section-093d1f611a1647568e885ddd842b8f78}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-43ccd77648784be4a259a723c3e1db40}

**Entrada (renameProjectParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyName`*` | `xsd:string` | Sim | Manuseie a empresa com o projeto que deseja renomear. |
| `*`projectHandle`*` | `xsd:string` | Sim | Manipule o projeto. |
| `*`projectName`*` | `xsd:string` | Sim | Novo nome do projeto. |

**Saída (renameProjectParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`projectHandle`*` | `xsd:string` | Sim | O identificador do projeto renomeado. |

## Exemplos {#section-a0a06d9244774795b695a10b92b2a5e7}

Essa amostra de código renomeia um projeto e retorna o identificador do projeto.

**Solicitação**

```java
<renameProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ApiTestProject</projectHandle>
   <projectName>ProjectTestAPI</projectName>
</renameProjectParam>
```

**Resposta**

```java
<renameProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
</renameProjectReturn>
```

