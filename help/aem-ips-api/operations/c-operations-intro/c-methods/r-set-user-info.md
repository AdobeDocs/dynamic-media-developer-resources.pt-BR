---
description: Define os atributos do usuário (por exemplo, nome, email, função etc.)
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: d8f8fe53-a874-4b77-9084-9a369862a672
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# setUserInfo{#setuserinfo}

Define os atributos do usuário (por exemplo, nome, email, função etc.)

Sintaxe

## Tipos de usuário autorizados {#section-6c28db5d15b3449492a73749e4f981ac}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-71b457921fe74acb862a1e112e550211}

**Entrada (setUserInfoParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Não | Identificador do usuário. |
| `*`firstName`*` | `xsd:string` | Sim | Nome. |
| `*`lastName`*` | `xsd:string` | Sim | Sobrenome. |
| `*`email`*` | `xsd:string` | Sim | Email do usuário. |
| `*`defaultRole`*` | `xsd:string` | Sim | Define a função de um usuário em cada empresa à qual ele pertence. Observe, no entanto, a função `IpsAdmin` substitui outras configurações por empresa. |
| `*`passwordExpires`*` | `xsd:dateTime` | Não | Defina a data de expiração da senha. |
| `*`isValid`*` | `xsd:boolean` | Sim | Determina se o usuário é um usuário IPS válido. |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Sim | Uma matriz de empresas lida com isso. |

**Saída (setUserInfoReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-272c103076fb4de0a53729e2f6bfb895}

**Solicitação**

```java
<setUserInfoParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <firstName>test</firstName>
   <lastName>test</lastName>
   <email>test@test.test</email>
   <defaultRole>IpsAdmin</defaultRole>
   <isValid>true</isValid>
</setUserInfoParam>
```

**Resposta**

Nenhum.
