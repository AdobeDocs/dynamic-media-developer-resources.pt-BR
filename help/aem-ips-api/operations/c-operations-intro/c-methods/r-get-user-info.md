---
description: Obtém informações sobre um usuário. Use o endereço de email e a senha de um usuário do sistema como credenciais para autorizar a solicitação. Caso contrário, a operação obterá informações sobre o usuário padrão.
solution: Experience Manager
title: getUserInfo
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 1981f25f-779e-4434-ab6b-0debb40521fe
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# getUserInfo{#getuserinfo}

Obtém informações sobre um usuário. Use o endereço de email e a senha de um usuário do sistema como credenciais para autorizar a solicitação. Caso contrário, a operação obterá informações sobre o usuário padrão.

Sintaxe

## Tipos de usuário autorizados {#section-1c42d78e914a4b84a946b3480f29b36a}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-e87b3cb743494719925c9458eed433b6}

**Entrada (getUserInfoParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Não | Manipule para o usuário cujas informações você deseja retornar. |
| `*`email`*` | `xsd:string` | Não | Endereço de email do usuário. |

**Saída (getUserInfoReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`userInfo`*` | `types:User` | Sim | O nome, sobrenome, endereço de email e função de um usuário, bem como se ele é válido e quando a senha do usuário expira. |

## Exemplos {#section-98d77a2e360a438dbe240099bea26a65}

Esta amostra de código retorna informações para o usuário padrão do IPS.

**Solicitação**

```java
<getUserInfoParam xmlns="http://www.scene7.com/IpsApi/xsd" /></getUserInfoParam>
```

**Resposta**

```java
<ns1:getUserInfoReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd"> 
   <ns1:userInfo> 
      <ns1:userHandle>3261|user@scene7.com</ns1:userHandle> 
      <ns1:firstName>FirstName</ns1:firstName> 
      <ns1:lastName>LastName</ns1:lastName> 
      <ns1:email>user@scene7.com</ns1:email> 
      <ns1:role>IpsAdmin</ns1:role> 
      <ns1:isValid>true</ns1:isValid> 
      <ns1:passwordExpires>2107-04-22T18:35:41.995Z</ns1:passwordExpires> 
   </ns1:userInfo> 
</ns1:getUserInfoReturn>
```
