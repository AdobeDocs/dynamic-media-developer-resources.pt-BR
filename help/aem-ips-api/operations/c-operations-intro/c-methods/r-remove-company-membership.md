---
description: Remove um usuário de uma ou mais empresas.
seo-description: Remove um usuário de uma ou mais empresas.
seo-title: removeCompanyMember
solution: Experience Manager
title: removeCompanyMember
topic: Scene7 Image Production System API
uuid: af57fde0-2297-41da-87bf-f063fc313264
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# removeCompanyMember{#removecompanymembership}

Remove um usuário de uma ou mais empresas.

Sintaxe

## Tipos de usuário autorizados {#section-e9a16c8a7d8d4845989a1488c9ca9c98}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-6dfce5e44d8a4799afd0c231a0b10463}

**Entrada (removeCompanyMembcingParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | Não | O identificador do usuário com a associação que você deseja remover. |
| ` *`companyHandleArray`*` | `types:HandleArray` | Sim | O identificador da empresa da qual você está removendo o usuário. |

**Saída (removeCompanyMemberReturn)**

A API IPS não retorna uma resposta para esta operação.

## Exemplos {#section-6b7903195e8647a1bd0502f87387ca62}

Esta amostra de código remove um usuário de uma empresa. Omita o identificador de usuário opcional para remover todos os usuários das empresas especificadas na matriz de identificador de empresa.

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
