---
description: Gera uma nova senha.
solution: Experience Manager
title: generatePassword
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 80e7642f-4aec-4ff0-a090-e59b7a065c39
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
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
