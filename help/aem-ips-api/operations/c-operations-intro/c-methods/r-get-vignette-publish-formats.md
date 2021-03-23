---
description: getVignettePublishFormats
solution: Experience Manager
title: getVignettePublishFormats
uuid: 2cf58002-5c4a-4391-85d4-4a67cb085afa
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '68'
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
| `*`companyHandle`*` | `xsd:string` | Sim | O nome da empresa. |

**Saída (getVignettePublishFormatsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`vinhetaFormatArray`*` | `types:VignettePublishFormatArray` | Sim | Matriz de formatos de publicação de vinheta. |

## Exemplos {#section-2cc32b27cc6243b7b3e273cc05996226}

Essa amostra de código retorna dois formatos de publicação de vinheta associados a uma empresa específica. As informações são retornadas em uma matriz, que é truncada por motivos de brevidade.

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

