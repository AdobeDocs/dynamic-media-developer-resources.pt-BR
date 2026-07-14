---
description: Cria um novo projeto.
solution: Experience Manager
title: createProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dd9c07df-9a8f-4b67-9838-31dd96fd127b
TQID: 'https://experienceleague.adobe.com/GKNImvhmX1bOepsV0-6QzgZr5jskJQlaqXCMIT5ue5M'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 0%

---

# createProject{#createproject}

Cria um novo projeto.

Sintaxe

## Tipos de usuário autorizados {#section-17878e2e4c3a44988c9a1af82c2ac319}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-8c741884eb54489bbaad0c444fee80b6}

**Entrada (createProjectParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | O identificador da empresa associada ao novo projeto. |
| projectName | `xsd:string` | Sim | Novo nome de projeto. |

**Saída (createProjectParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| projectHandle | `xsd:string` | Sim | O identificador para o novo projeto. |

## Exemplos {#section-a0cd532b67e346d088fbec141231a0e5}

Esta amostra de código cria um projeto chamado `ApiTestProject` em uma empresa especificada por seu identificador. A resposta retorna o identificador para o projeto.

**Solicitação**

```java
<createProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectName>ApiTestProject</projectName>
</createProjectParam>
```

```java
<createProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ApiTestProject</projectHandle>
</createProjectReturn>
```

