---
description: Retorna os usuários de uma empresa especificada por um identificador de empresa.
solution: Experience Manager
title: getCompanyMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: da5e5a48-2e0b-4ccc-a71e-b5b746484d4a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '89'
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
| companyHandle | `xsd:string` | Sim | O identificador da empresa cujos membros você deseja obter. |
| includeInvalid | `xsd:boolean` | Sim | Inclua empresas inválidas. |

**Saída (getCompanyMembersReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| memberArray | `types:CompanyMemberArray` | Sim | Matriz de associações de usuário. |

## Exemplos {#section-39d8cf3653fd4fe8b842caabac9dedfc}

Esta amostra de código retorna todos os membros de uma empresa em uma matriz de usuário. A resposta foi truncada por brevidade.

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
