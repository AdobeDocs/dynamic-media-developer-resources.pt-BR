---
description: Exclui um formato de publicação de vinheta.
solution: Experience Manager
title: deleteVignettePublishFormat
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '82'
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
