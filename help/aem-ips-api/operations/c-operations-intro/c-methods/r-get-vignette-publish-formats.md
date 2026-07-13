---
description: getVignettePublishFormats
solution: Experience Manager
title: getVignettePublishFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6e56d68e-b5cf-4044-9c58-f8221fa4490f
TQID: 'https://experienceleague.adobe.com/2boU6c0m2JZ6kLBXvNVtb0udCXQAP4u8hrFIGk0Pezs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 61
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

