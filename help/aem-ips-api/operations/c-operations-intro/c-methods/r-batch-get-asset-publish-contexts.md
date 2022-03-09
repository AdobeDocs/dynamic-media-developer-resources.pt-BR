---
description: Retorna os contextos de publicação para ativos marcados para publicação.
solution: Experience Manager
title: batchGetAssetPublishContexts
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ba1f62a7-2698-4300-b6de-6d07ac764b0c
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# batchGetAssetPublishContexts{#batchgetassetpublishcontexts}

Retorna os contextos de publicação para ativos marcados para publicação.

Sintaxe

## Tipos de usuário autorizados {#section-d5362ca8a6ab42949cd648ba38dbf2f8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>* O usuário deve ter acesso de leitura para retornar os ativos.
>* Todos os usuários têm acesso à empresa compartilhada.
>


## Parâmetros {#section-1742fcb196224545b270eb8241f757a8}

**Entrada (batchGetAssetPublishContextsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | Manipule a empresa. |
| assetHandleArray | ` `tipos:HandleArray&quot; | Sim | Uma lista de ativos que você deseja consultar para contextos ativos (marcados para publicação). |

**Saída (batchGetAssetPublishContextsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| assetPublishContextsArray | `types:assetPublishContextsArray` | Sim | Uma matriz de contextos de publicação em que cada ativo é marcado para publicação. |

## Exemplos {#section-457f6809ccfa425b9a0976313d613f4e}

**Solicitação**

```java {.line-numbers}
<batchGetAssetPublishContextsParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetHandleArray>
    <items>a|27007</items>
    <items>a|27008</items>
  </assetHandleArray>
</batchGetAssetPublishContextsParam>
```

**Resposta**

```java {.line-numbers}
<batchGetAssetPublishContextsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <assetPublishContextsArray>
    <items>
      <assetHandle>a|27007</assetHandle>
      <publishContextArray>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <contextName>ImageServing</contextName>
          <contextType>ImageServing</contextType>
        </items>
      </publishContextArray>
    </items>
    <items>
      <assetHandle>a|27008</assetHandle>
      <publishContextArray>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <contextName>Video</contextName>
          <contextType>Video</contextType>
        </items>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <contextName>ImageRendering</contextName>
          <contextType>ImageRendering</contextType>
        </items>
      </publishContextArray>
    </items>
  </assetPublishContextsArray>
</batchGetAssetPublishContextsReturn>
```
