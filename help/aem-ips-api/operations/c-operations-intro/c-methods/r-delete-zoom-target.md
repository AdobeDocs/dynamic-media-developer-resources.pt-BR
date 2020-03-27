---
description: Exclui um público alvo de zoom.
seo-description: Exclui um público alvo de zoom.
seo-title: deleteZoomTarget
solution: Experience Manager
title: deleteZoomTarget
topic: Scene7 Image Production System API
uuid: 01a9321f-89a9-4263-937b-b0b49fe2fb81
translation-type: tm+mt
source-git-commit: d3766bba78cd1051538ff6a94f61ba61e989f1a5

---


# deleteZoomTarget{#deletezoomtarget}

Exclui um público alvo de zoom.

## Tipos de usuário autorizados {#section-09ca82bc817e49048271c5cba545702e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>O usuário deve ter acesso de leitura e gravação ao ativo.

## Parâmetros {#section-225330a45e7a408f8375e084677d9cb1}

**Entrada (deleteZoomTargetParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sim | A alça da empresa à qual o público alvo de zoom pertence. |
| ` *`zoomTargetHandle`*` | `xsd:string` | Sim | A alça do público alvo de zoom a ser excluído. |

**Saída (deleteZoomTargetParam)**

A API IPS não retorna uma resposta para esta operação.

## Example {#section-a35857a5ca884357a879f7ba6cf985fe}

Esta amostra de código exclui um público alvo de zoom de uma empresa.

**Solicitação**

```java
<ns1:deleteZoomTargetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:zoomTargetHandle>34194|9|301</ns1:zoomTargetHandle>
</ns1:deleteZoomTargetParam>
```

**Resposta**

Nenhum.
