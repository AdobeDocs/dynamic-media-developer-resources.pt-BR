---
description: Remove um usuário de uma ou mais empresas.
solution: Experience Manager
title: removeCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1cb9a286-48a0-4542-a80a-c97fd973474e
TQID: 'https://experienceleague.adobe.com/5jjL8MnUtL046oSej3HErZB9hrD-ueEBC5-h9vD92HM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 100
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
| userHandle | `xsd:string` | Não | O identificador para o usuário com a associação que você deseja remover. |
| companyHandleArray | `types:HandleArray` | Sim | O identificador da empresa da qual você está removendo o usuário. |

**Saída (removeCompanyMembershipReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-6b7903195e8647a1bd0502f87387ca62}

Esta amostra de código remove um usuário de uma empresa. Omita o identificador de usuário opcional para remover todos os usuários das empresas especificadas na matriz de identificadores de empresa.

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

