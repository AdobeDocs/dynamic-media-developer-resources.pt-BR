---
description: Gera uma nova senha.
seo-description: Gera uma nova senha.
seo-title: generatePassword
solution: Experience Manager
title: generatePassword
topic: Dynamic Media Image Production System API
uuid: e3367bfc-d437-4a61-83e8-69830154dc61
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '64'
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
| `*`password`*` | `xsd:string` | Sim | Uma nova senha. |

## Exemplos {#section-f580fefdccec46fe95359e3aef0ed17f}

Esta amostra de código gera uma senha. É incomum porque a solicitação é simplesmente um parâmetro sem quaisquer elementos ou valores delimitados. O IPS retorna uma senha forte.

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

