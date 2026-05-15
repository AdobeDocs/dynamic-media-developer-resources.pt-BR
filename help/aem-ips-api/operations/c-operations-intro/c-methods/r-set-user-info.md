---
description: Define os atributos do usuário (por exemplo, nome, email, função e assim por diante).
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d8f8fe53-a874-4b77-9084-9a369862a672
TQID: 'https://experienceleague.adobe.com/JzJv4nEeWfbY-Wp-qkEq883dlTqaRm9Fc-UvDa70dOg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 114
ht-degree: 0%

---

# setUserInfo{#setuserinfo}

Define os atributos do usuário (por exemplo, nome, email, função e assim por diante).

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
| userHandle | `xsd:string` | Não | Identificador de usuário. |
| firstName | `xsd:string` | Sim | Nome. |
| lastName | `xsd:string` | Sim | Sobrenome. |
| email | `xsd:string` | Sim | Email do usuário. |
| defaultRole | `xsd:string` | Sim | Define a função de um usuário em cada empresa à qual ele pertence. No entanto, observe que a função `IpsAdmin` substitui outras configurações por empresa. |
| passwordExpires | `xsd:dateTime` | Não | Defina a data de expiração da senha do. |
| isValid | `xsd:boolean` | Sim | Determina se o usuário é um usuário de IPS válido. |
| memberArray | `types:CompanyMembershipUpdateArray` | Sim | Uma matriz de manipuladores de empresa. |

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
