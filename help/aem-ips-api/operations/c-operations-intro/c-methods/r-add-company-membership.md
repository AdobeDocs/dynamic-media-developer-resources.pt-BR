---
description: Adiciona um usuário a uma ou mais empresas.
solution: Experience Manager
title: addCompanyMembership
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 6efef4fb-f2e5-4c41-b739-a36ac2f17884
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---

# addCompanyMembership{#addcompanymembership}

Adiciona um usuário a uma ou mais empresas.

Sintaxe

## Tipos de usuário autorizados {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-0e925b91d63e48aa91f0b0014e6a0cab}

**Entrada (addCompanyMembershipParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Não | O identificador do usuário cuja associação você deseja adicionar. |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Sim | Uma matriz de empresas para as quais você está adicionando o usuário. |

**Saída (addCompanyMembershipReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-5469f88bac7047cca131faa6b021e437}

Este exemplo usa `*`companyHandleArray`*` para adicionar um usuário a uma única empresa.

**Solicitação**

```java
<ns1:addCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      </ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addCompanyMembershipParam>
```

**Resposta**

Nenhum.
