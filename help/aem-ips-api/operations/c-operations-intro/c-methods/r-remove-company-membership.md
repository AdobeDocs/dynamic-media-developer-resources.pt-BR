---
description: Remove um usuário de uma ou mais empresas.
solution: Experience Manager
title: removeCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1cb9a286-48a0-4542-a80a-c97fd973474e
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---

# removeCompanyMembership{#removecompanymembership}

Remove um usuário de uma ou mais empresas.

Sintaxe

## Tipos de usuário autorizados {#section-e9a16c8a7d8d4845989a1488c9ca9c98}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-6dfce5e44d8a4799afd0c231a0b10463}

**Entrada (removeCompanyMembershipParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| userHandle | `xsd:string` | Não | O nome do usuário com a associação que você deseja remover. |
| companyHandleArray | `types:HandleArray` | Sim | O identificador da empresa da qual você está removendo o usuário. |

**Saída (removeCompanyMembershipReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-6b7903195e8647a1bd0502f87387ca62}

Essa amostra de código remove um usuário de uma empresa. Omita o identificador de usuário opcional para remover todos os usuários das empresas especificadas na matriz de controle da empresa.

**Solicitação**

```java
<ns1:removeCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:removeCompanyMembershipParam>
```

**Resposta**

Nenhum.
