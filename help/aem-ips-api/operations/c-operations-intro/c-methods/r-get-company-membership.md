---
description: Obtém as associações de um usuário em uma matriz de empresa.
seo-description: Obtém as associações de um usuário em uma matriz de empresa.
seo-title: getCompanyMember
solution: Experience Manager
title: getCompanyMember
topic: Dynamic Media Image Production System API
uuid: fb3dfe29-4292-4ab2-8015-36c4930a9c05
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---


# getCompanyMember{#getcompanymembership}

Obtém as associações de um usuário em uma matriz de empresa.

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

**Entrada (getCompanyMembcingParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Não | O identificador do usuário cujas associações você deseja obter. |

**Saída (getCompanyMemberReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`subscriptionArray`*` | `types:CompanyMembershipArray` | Sim | Matriz de associações empresas. |

## Exemplos {#section-e4958d104ea344a4a79f57d07b46eba7}

Essa amostra de código obtém um identificador de usuário e obtém todas as associações de empresa do usuário em um storage. A resposta foi truncada para brevidade.

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

