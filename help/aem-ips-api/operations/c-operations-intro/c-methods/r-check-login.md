---
description: Verifica se um usuário com uma empresa específica (identificada pelo identificador), endereço de email e senha pode fazer logon.
solution: Experience Manager
title: checkLogin
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1f96f376-574c-464b-9c89-c215f6454b81
TQID: 'https://experienceleague.adobe.com/5o2geLVIOZLg7tmKrHueWkzjf4EhXedAJ5qvWxTzjB0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 145
ht-degree: 0%

---

# checkLogin{#checklogin}

Verifica se um usuário com uma empresa específica (identificada pelo identificador), endereço de email e senha pode fazer logon.

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
| companyHandle | `xsd:string` | Não | O identificador da empresa que contém o usuário. |
| email | `xsd:string` | Sim | O endereço de email do usuário. |
| senha | `xsd:string` | Sim | A senha do usuário. |

**Saída (checkLoginParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| status | `xsd:string` | Sim | Status de logon do usuário. |

## Exemplos {#section-23f90100a9d94bc7b4045634cccd1b98}

Este código de exemplo usa um parâmetro de identificador de empresa, endereço de email e uma senha para determinar se um usuário pode fazer logon no IPS. Se o usuário *puder* fazer logon, esse método retornará a cadeia de caracteres `ValidLogin`. Se o usuário *não puder* fazer logon, esse método retornará a cadeia de caracteres `InvalidLogin`.

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

