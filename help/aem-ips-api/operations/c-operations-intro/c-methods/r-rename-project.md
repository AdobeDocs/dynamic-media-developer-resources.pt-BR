---
description: Renomeia um projeto.
solution: Experience Manager
title: renameProject
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1bf74ebf-1fce-408b-9953-7fdf2ae9d10b
TQID: 'https://experienceleague.adobe.com/FjPL1Xn4QAYYCdyeYKA1MiQVay988g-sbuiHpazhcMM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 71
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
| companyName | `xsd:string` | Sim | Processe a empresa com o projeto que você deseja renomear. |
| projectHandle | `xsd:string` | Sim | Identificador para o projeto. |
| projectName | `xsd:string` | Sim | Novo nome de projeto. |

**Saída (renameProjectParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| projectHandle | `xsd:string` | Sim | O identificador do projeto renomeado. |

## Exemplos {#section-a0a06d9244774795b695a10b92b2a5e7}

Esta amostra de código renomeia um projeto e retorna o identificador do projeto.

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
