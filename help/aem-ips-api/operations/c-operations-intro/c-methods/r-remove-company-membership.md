---
description: Remove um usuário de uma ou mais empresas.
seo-description: Remove um usuário de uma ou mais empresas.
seo-title: removeCompanyMembership
solution: Experience Manager
title: removeCompanyMembership
uuid: af57fde0-2297-41da-87bf-f063fc313264
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '116'
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
| `*`userHandle`*` | `xsd:string` | Não | O nome do usuário com a associação que você deseja remover. |
| `*`companyHandleArray`*` | `types:HandleArray` | Sim | O identificador da empresa da qual você está removendo o usuário. |

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
