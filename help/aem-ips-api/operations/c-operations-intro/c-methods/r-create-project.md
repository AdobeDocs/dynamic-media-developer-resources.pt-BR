---
description: Cria um novo projeto.
solution: Experience Manager
title: createProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dd9c07df-9a8f-4b67-9838-31dd96fd127b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '76'
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
| projectName | `xsd:string` | Sim | Novo nome do projeto. |

**Saída (createProjectParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| projectHandle | `xsd:string` | Sim | O identificador do novo projeto. |

## Exemplos {#section-a0cd532b67e346d088fbec141231a0e5}

Essa amostra de código cria um projeto chamado `ApiTestProject` numa empresa especificada pelo seu identificador. A resposta retorna o identificador para o projeto.

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
