---
description: getVignettePublishFormats
solution: Experience Manager
title: getVignettePublishFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6e56d68e-b5cf-4044-9c58-f8221fa4490f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 0%

---

# getVignettePublishFormats{#getvignettepublishformats}

Sintaxe

## Tipos de usuário autorizados {#section-1f5e2f74aef8408e89ed9ccac8b5b9bc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-ba28150e6d8c4aa0b4ec72451ba7bc71}

**Entrada (getVignettePublishFormatsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | O identificador da empresa. |

**Saída (getVignettePublishFormatsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| vignetteFormatArray | `types:VignettePublishFormatArray` | Sim | Matriz de formatos de publicação de vinheta. |

## Exemplos {#section-2cc32b27cc6243b7b3e273cc05996226}

Essa amostra de código retorna dois formatos de publicação de vinheta associados a uma empresa específica. As informações são retornadas em uma matriz, que é truncada por brevidade.

**Solicitação**

```java
<getVignettePublishFormatsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
</getVignettePublishFormatsParam>
```

**Resposta**

```java
<getVignettePublishFormatsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatArray>
      <items>
         <companyHandle>c|21</companyHandle>
         <vignetteFormatHandle>v|21|281</vignetteFormatHandle>
         <name>APIcreateVignettePublishFormat</name>
         ...
      </items>
   </vignetteFormatArray>
</getVignettePublishFormatsReturn>
```
