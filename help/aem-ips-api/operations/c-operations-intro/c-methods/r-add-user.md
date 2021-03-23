---
description: Cria uma conta de usuário e a adiciona a uma ou mais empresas.
solution: Experience Manager
title: addUser
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---


# addUser{#adduser}

Cria uma conta de usuário e a adiciona a uma ou mais empresas.

Ao adicionar um usuário a várias empresas, especifique essas empresas pelo controle da empresa em `companyHandleArray`. Essa operação retorna o identificador ao usuário que você acabou de adicionar.

## Tipos de usuário autorizados {#section-126ad42f844444fea11ecf8ad01fe1ec}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-40390a512e314b8d80ecffbb7729f6fb}

**Entrada (addUserParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`firstName`*` | `xsd:string` | Sim | O nome do usuário. |
| `*`lastName`*` | `xsd:string` | Sim | O sobrenome do usuário. |
| `*`email`*` | `xsd:string` | Sim | O endereço de email do usuário. |
| `*`defaultRole`*` | `xsd:string` | Sim | Define a função de um usuário em cada empresa à qual ele pertence. Observe, no entanto, a função `IpsAdmin` substitui outras configurações por empresa. |
| `*`senha`*` | `xsd:string` | Sim | Define a senha do usuário |
| `*`passwordExpires`*` | `xsd:dateTime` | Não | Define o período de expiração da senha. Forneça o fuso horário ao transmitir a solicitação. Os fusos horários são ajustados para Hora central. |
| `*`isValid`*` | `xsd:boolean` | Sim | Determina se o usuário é válido. |
| `*`membershipArray`*` | `xsd:CompanyMembershipUpdateArray` | Sim | Uma matriz de empresas lida com isso. |

**Saída (addUserParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Sim | O identificador para o usuário. |

## Exemplos {#section-2547cef622734b71919eef849960b5cb}

A API do IPS retorna um elemento de identificador de usuário que especifica o novo usuário.

**Solicitação**

```java
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

```java
<ns1:addUserReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>525s|juser@scene7.com</ns1:userHandle>
</ns1:addUserReturn>
```

