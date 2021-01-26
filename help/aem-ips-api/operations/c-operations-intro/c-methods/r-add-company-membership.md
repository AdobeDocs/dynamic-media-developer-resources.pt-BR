---
description: Adiciona um usuário a uma ou mais empresas.
solution: Experience Manager
title: addCompanyMember
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# addCompanyMember{#addcompanymembership}

Adiciona um usuário a uma ou mais empresas.

Sintaxe

## Tipos de usuário autorizados {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-0e925b91d63e48aa91f0b0014e6a0cab}

**Entrada (addCompanyMembcingParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Não | O identificador do usuário cuja associação você deseja adicionar. |
| `*`subscriptionArray`*` | `types:CompanyMembershipUpdateArray` | Sim | Uma matriz de empresas à qual você está adicionando o usuário. |

**Saída (addCompanyMemberReturn)**

A API IPS não retorna uma resposta para esta operação.

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
