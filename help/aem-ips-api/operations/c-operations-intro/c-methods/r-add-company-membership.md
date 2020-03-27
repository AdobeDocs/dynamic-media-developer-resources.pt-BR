---
description: Adiciona um usuário a uma ou mais empresas.
seo-description: Adiciona um usuário a uma ou mais empresas.
seo-title: addCompanyMember
solution: Experience Manager
title: addCompanyMember
topic: Scene7 Image Production System API
uuid: be55041c-fc4e-46e8-bd2c-81b5931406f5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`userHandle`*` | `xsd:string` | Não | O identificador do usuário cuja associação você deseja adicionar. |
| ` *`subscriptionArray`*` | `types:CompanyMembershipUpdateArray` | Sim | Uma matriz de empresas à qual você está adicionando o usuário. |

**Saída (addCompanyMemberReturn)**

A API IPS não retorna uma resposta para esta operação.

## Exemplos {#section-5469f88bac7047cca131faa6b021e437}

Este exemplo usa ` *`companyHandleArray`*` para adicionar um usuário a uma única empresa.

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
