---
description: Define a associação de um usuário em uma ou mais empresas.
seo-description: Define a associação de um usuário em uma ou mais empresas.
seo-title: setCompanyMember
solution: Experience Manager
title: setCompanyMember
topic: Dynamic Media Image Production System API
uuid: 34c9d457-bc2e-4186-8a8f-50388410640a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---


# setCompanyMember{#setcompanymembership}

Define a associação de um usuário em uma ou mais empresas.

Sintaxe

## Tipos de usuário autorizados {#section-0cbcc78cfee64c2baf66f29cce6d0a65}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-3930dc6a016140178631083563598104}

**Entrada (setCompanyMembcingParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`userHandle`*` | `xsd:sting` | Não | Identificador do usuário. |
| `*`subscriptionArray`*` | `types:CompanyMembershipUpdateArray` | Sim | Matriz de empresas. |

**Saída (setCompanyMemberParam)**

A API IPS não retorna uma resposta para esta operação.

## Exemplos {#section-862c0cc32ce0407ab248028e690a8386}

Essa amostra de código adiciona um usuário a uma empresa. Especifique várias empresas na matriz de empresa, se necessário.

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
