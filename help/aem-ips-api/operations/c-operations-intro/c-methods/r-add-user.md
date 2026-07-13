---
description: Cria uma conta de usuário e a adiciona a uma ou mais empresas.
solution: Experience Manager
title: addUser
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: aed39e73-f528-4c26-8f62-c3d796e9101a
TQID: 'https://experienceleague.adobe.com/dR1bVB3TeSd9qnnVPrp0YIg3-kS51rPHnVWVVrhZt8s'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 177
ht-degree: 0%

---

# addUser{#adduser}

Cria uma conta de usuário e a adiciona a uma ou mais empresas.

Ao adicionar um usuário a várias empresas, especifique essas empresas pelos identificadores de empresa em `companyHandleArray`. Esta operação retorna o identificador para o usuário que você acabou de adicionar.

## Tipos de usuário autorizados {#section-126ad42f844444fea11ecf8ad01fe1ec}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-40390a512e314b8d80ecffbb7729f6fb}

**Entrada (addUserParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| firstName | `xsd:string` | Sim | O nome do usuário. |
| lastName | `xsd:string` | Sim | O sobrenome do usuário. |
| email | `xsd:string` | Sim | O endereço de email do usuário. |
| defaultRole | `xsd:string` | Sim | Define a função de um usuário em cada empresa à qual ele pertence. No entanto, observe que a função `IpsAdmin` substitui outras configurações por empresa. |
| senha | `xsd:string` | Sim | Define a senha do usuário |
| passwordExpires | `xsd:dateTime` | Não | Define o período de expiração da senha. Forneça o fuso horário ao transmitir a solicitação. Os fusos horários são ajustados para a Hora central. |
| isValid | `xsd:boolean` | Sim | Determina se o usuário é válido. |
| memberArray | `xsd:CompanyMembershipUpdateArray` | Sim | Uma matriz de manipuladores de empresa. |

**Saída (addUserParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| userHandle | `xsd:string` | Sim | O identificador para o usuário. |

## Exemplos {#section-2547cef622734b71919eef849960b5cb}

A API IPS retorna um elemento de identificador de usuário que especifica o novo usuário.

**Solicitação**

```java {.line-numbers}
<ns1:addUserParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:firstName>Joe</ns1:firstName>
   <ns1:lastName>User</ns1:lastName>
   <ns1:email>juser@adobe.com</ns1:email>
   <ns1:defaultRole>TrialSiteUser</ns1:role>
   <ns1:password>passw0rd</ns1:password>
   <ns1:isValid>true</ns1:isValid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addUserParam>
```

**Resposta**

```java {.line-numbers}
<ns1:addUserReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>525s|juser@scene7.com</ns1:userHandle>
</ns1:addUserReturn>
```

