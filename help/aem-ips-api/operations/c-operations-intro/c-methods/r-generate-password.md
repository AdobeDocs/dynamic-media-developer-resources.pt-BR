---
description: Gera uma nova senha.
seo-description: Gera uma nova senha.
seo-title: generatePassword
solution: Experience Manager
title: generatePassword
uuid: e3367bfc-d437-4a61-83e8-69830154dc61
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---


# generatePassword{#generatepassword}

Gera uma nova senha.

Sintaxe

## Tipos de usuário autorizados {#section-88f7dc11e5c74be281399d8f2e3c9555}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-d516615c906240819a284786efb19863}

**Entrada (generatePasswordParam)**

Nenhum.

**Saída (generatePasswordParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`senha`*` | `xsd:string` | Sim | Uma nova senha. |

## Exemplos {#section-f580fefdccec46fe95359e3aef0ed17f}

Essa amostra de código gera uma senha. Isso é incomum porque a solicitação é simplesmente um parâmetro sem elementos ou valores delimitados. O IPS retorna uma senha forte.

**Solicitação**

```java
<generatePasswordParam xmlns="http://www.scene7.com/IpsApi/xsd">
</generatePasswordParam>
```

**Resposta**

```java
<generatePasswordReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <password>1\7aQRn]</password>
</generatePasswordReturn>
```

