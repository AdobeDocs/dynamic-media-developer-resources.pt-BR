---
description: Exclui um formato de publicação de vinheta.
solution: Experience Manager
title: deleteVignettePublishFormat
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: a437cb47-c45c-41a0-8499-53e4c2ae3164
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# deleteVignettePublishFormat{#deletevignettepublishformat}

Exclui um formato de publicação de vinheta.

## Tipos de usuário autorizados {#section-a127680d6b53462daaf2579d6f6fe5a8}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-789625ba29df4b5f880914d4c64f77ce}

**Entrada (deleteVignettePublishFormatParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa à qual a vinheta pertence. |
| `*`vinhetaFormatarIdentificador`*` | `xsd:string` | Sim | O identificador para o formato de publicação da vinheta a ser excluído. |

**Saída (deleteVignettePublishFormatParam)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-5ab2a314ad4c41ac8b3a24eaea7d8585}

Essa amostra de código exclui um formato de publicação de vinheta especificado por seu identificador.

**Solicitação**

```java
<deleteVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</deleteVignettePublishFormatParam>
```

**Resposta**

Nenhum.
