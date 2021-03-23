---
description: Adiciona um usuário a uma ou mais empresas.
solution: Experience Manager
title: addCompanyMembership
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '90'
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
