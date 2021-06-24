---
description: Define a associação de um usuário em uma ou mais empresas.
solution: Experience Manager
title: setCompanyMembership
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 43144c75-1d83-4e1d-8319-c3275d349a2f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# setCompanyMembership{#setcompanymembership}

Define a associação de um usuário em uma ou mais empresas.

Sintaxe

## Tipos de usuário autorizados {#section-0cbcc78cfee64c2baf66f29cce6d0a65}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-3930dc6a016140178631083563598104}

**Entrada (setCompanyMembershipParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`userHandle`*` | `xsd:sting` | Não | Identificador do usuário. |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Sim | Matriz de empresas. |

**Saída (setCompanyMembershipParam)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-862c0cc32ce0407ab248028e690a8386}

Essa amostra de código adiciona um usuário a uma empresa. Especifique várias empresas no conjunto de controle da empresa, se necessário.

**Solicitação**

```java
<ns1:setCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle>
   <ns1:companyHandleArray>
      <ns1:items>137</ns1:items>
   </ns1:companyHandleArray>
</ns1:setCompanyMembershipParam>
```

**Resposta**

Nenhum.
