---
description: Verifica se um usuário com uma empresa específica (identificada por identificador), endereço de email e senha pode fazer logon.
seo-description: Verifica se um usuário com uma empresa específica (identificada por identificador), endereço de email e senha pode fazer logon.
seo-title: checkLogin
solution: Experience Manager
title: checkLogin
uuid: 69f9e5f6-50c2-403d-93b2-b84a01f512a9
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---


# checkLogin{#checklogin}

Verifica se um usuário com uma empresa específica (identificada por identificador), endereço de email e senha pode fazer logon.

>[!NOTE]
>
>Se o identificador da empresa for omitido, esse método verificará o logon do usuário padrão.

## Tipos de usuário autorizados {#section-df8b26b550854f899948276adaca083a}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-1ad4c0b4803b4388aedd655030676cb3}

**Entrada (checkLoginParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Não | O identificador para a empresa que contém o usuário. |
| `*`email`*` | `xsd:string` | Sim | O endereço de email do usuário. |
| `*`senha`*` | `xsd:string` | Sim | A senha do usuário. |

**Saída (checkLoginParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`status`*` | `xsd:string` | Sim | Status de logon do usuário. |

## Exemplos {#section-23f90100a9d94bc7b4045634cccd1b98}

Este código de exemplo usa um parâmetro de identificador da empresa, um endereço de email e uma senha para determinar se um usuário pode fazer logon no IPS. Se o usuário *pode* fazer logon, esse método retornará a string, `ValidLogin`. Se o usuário *não puder* fazer logon, esse método retornará a string, `InvalidLogin`.

**Solicitação**

```java
<ns1:checkLoginParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>137</ns1:companyHandle>
   <ns1:email>juser3@scene7.com</ns1:email>
   <ns1:password>welcome</ns1:password>
</ns1:checkLoginParam>
```

**Resposta**

```java
<ns1:checkLoginReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:status>InvalidLogin</ns1:status>
</ns1:checkLoginReturn>
```

