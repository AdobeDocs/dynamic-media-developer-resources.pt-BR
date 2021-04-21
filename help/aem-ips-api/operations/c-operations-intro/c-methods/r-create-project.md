---
description: Cria um novo projeto.
solution: Experience Manager
title: createProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
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
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa associada ao novo projeto. |
| `*`projectName`*` | `xsd:string` | Sim | Novo nome do projeto. |

**Saída (createProjectParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`projectHandle`*` | `xsd:string` | Sim | O identificador do novo projeto. |

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

