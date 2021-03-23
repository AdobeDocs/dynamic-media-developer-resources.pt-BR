---
description: Obtém as associações de um usuário em um array de empresas.
seo-description: Obtém as associações de um usuário em um array de empresas.
seo-title: getCompanyMembership
solution: Experience Manager
title: getCompanyMembership
uuid: fb3dfe29-4292-4ab2-8015-36c4930a9c05
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---


# getCompanyMembership{#getcompanymembership}

Obtém as associações de um usuário em um array de empresas.

Sintaxe

## Tipos de usuário autorizados {#section-f8bba547e1f648648be99dc48fd72b5d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-8745c360c3e1400a88e9bdb26bcb93de}

**Entrada (getCompanyMembershipParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Não | O identificador do usuário cujas associações você deseja obter. |

**Saída (getCompanyMembershipReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`membershipArray`*` | `types:CompanyMembershipArray` | Sim | Matriz de associações a empresas. |

## Exemplos {#section-e4958d104ea344a4a79f57d07b46eba7}

Essa amostra de código obtém um identificador de usuário e todas as associações de empresa do usuário em uma matriz. A resposta foi truncada por brevidade.

**Solicitação**

```java
<ns1:getCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
</ns1:getCompanyMembershipParam>
```

**Resposta**

```java
<getCompanyMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <membershipArray>
      <items>
         <companyHandle>48</companyHandle>
         <name>AIR</name>
         <rootPath>AIR/</rootPath>
         <expires>2101-01-31T23:00:00.485-08:00</expires>
      </items>
      ...
    </membershipArray>
</getCompanyMembershipReturn>
```

