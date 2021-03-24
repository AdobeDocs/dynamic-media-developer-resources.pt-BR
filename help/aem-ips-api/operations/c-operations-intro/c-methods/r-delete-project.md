---
description: Exclui um projeto de uma empresa. Os links entre os ativos e o projeto são quebrados, mas os ativos não são excluídos do IPS.
solution: Experience Manager
title: deleteProject
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---


# deleteProject{#deleteproject}

Exclui um projeto de uma empresa. Os links entre os ativos e o projeto são quebrados, mas os ativos não são excluídos do IPS.

Sintaxe

## Tipos de usuário autorizados {#section-d8a70e23c68d426e9af1357b978ae2f0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-00d1e00dd5014513a52b4e6b4f61de62}

**Entrada (deleteProjectParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyName`*` | `xsd:string` | Sim | O nome da empresa associada ao projeto. |
| `*`projectHandle`*` | `xsd:string` | Sim | O identificador do projeto a ser excluído. |

**Saída (deleteProjectReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-e38507f1f7ec41b9a625f47390490254}

Esta amostra de código usa o identificador da empresa e o identificador do projeto como campos no deleteProjectParam enviados ao servidor de serviços Web IPS para excluir o projeto.

**Solicitação**

```java
<deleteProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
<projectHandle>p|6|ProjectTestAPI</projectHandle></deleteProjectParam>
```

**Resposta**

Nenhum.
