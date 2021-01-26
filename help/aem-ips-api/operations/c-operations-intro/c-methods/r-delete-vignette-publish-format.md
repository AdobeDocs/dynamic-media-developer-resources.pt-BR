---
description: Exclui um formato de publicação de vinheta.
seo-description: Exclui um formato de publicação de vinheta.
seo-title: deleteVignettePublishFormat
solution: Experience Manager
title: deleteVignettePublishFormat
topic: Dynamic Media Image Production System API
uuid: 3c8148d5-dec6-4ffa-8ab8-2cd70811ada6
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '81'
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
| `*`companyHandle`*` | `xsd:string` | Sim | A alça da empresa à qual a vinheta pertence. |
| `*`vignetteFormatHandle`*` | `xsd:string` | Sim | O identificador do formato de publicação de vinheta a ser excluído. |

**Saída (deleteVignettePublishFormatParam)**

A API IPS não retorna uma resposta para esta operação.

## Exemplos {#section-5ab2a314ad4c41ac8b3a24eaea7d8585}

Esta amostra de código exclui um formato de publicação de vinheta especificado por seu identificador.

**Solicitação**

```java
<deleteVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</deleteVignettePublishFormatParam>
```

**Resposta**

Nenhum.
