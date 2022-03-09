---
description: Renomeia um projeto.
solution: Experience Manager
title: renameProject
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1bf74ebf-1fce-408b-9953-7fdf2ae9d10b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '71'
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
| companyName | `xsd:string` | Sim | Lide com a empresa com o projeto que deseja renomear. |
| projectHandle | `xsd:string` | Sim | Manipule o projeto. |
| projectName | `xsd:string` | Sim | Novo nome do projeto. |

**Saída (renameProjectParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| projectHandle | `xsd:string` | Sim | O identificador do projeto renomeado. |

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
