---
description: Retorna os usuários de uma empresa especificada por um identificador de empresa.
seo-description: Retorna os usuários de uma empresa especificada por um identificador de empresa.
seo-title: getCompanyMembers
solution: Experience Manager
title: getCompanyMembers
topic: Dynamic Media Image Production System API
uuid: 45e2d040-a70a-46f4-863a-633ddabcbcf6
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# getCompanyMembers{#getcompanymembers}

Retorna os usuários de uma empresa especificada por um identificador de empresa.

Sintaxe

## Tipos de usuário autorizados {#section-b2bc2fa0cc944cea8be82524838307cc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-5602e4d6f2214e398e6a804e61f1a088}

**Entrada (getCompanyMembersParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa cujos membros você deseja obter. |
| `*`includeInvalid`*` | `xsd:boolean` | Sim | Incluir empresas inválidas. |

**Saída (getCompanyMembersReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`memberArray`*` | `types:CompanyMemberArray` | Sim | Matriz de associações de usuários. |

## Exemplos {#section-39d8cf3653fd4fe8b842caabac9dedfc}

Essa amostra de código retorna todos os membros de uma empresa em um storage de usuários. A resposta foi truncada para brevidade.

**Solicitação**

```java
<ns1:getCompanyMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:includeInvalid>false</ns1:includeInvalid>
</ns1:getCompanyMembersParam>
```

**Resposta**

```java
<getCompanyMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <memberArray>
      <items>
         <userHandle>66|pbayol@adobe.com</userHandle>
         <firstName>Peter</firstName>
         <lastName>Bayol</lastName>
         <email>pbayol@adobe.com</email>
         <role>IpsAdmin</role>
         <isValid>true</isValid>
         <passwordExpires>2107-07-25T23:12:49.472-07:00</passwordExpires>
      </items>
      ...
   </memberArray>
</getCompanyMembersReturn>
```

