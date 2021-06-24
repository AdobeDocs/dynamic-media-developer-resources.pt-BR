---
description: Exclui um direcionamento de zoom.
solution: Experience Manager
title: deleteZoomTarget
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: fa1f7cf8-038a-4fa8-b869-12ce4b2ad41f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# deleteZoomTarget{#deletezoomtarget}

Exclui um direcionamento de zoom.

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
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa à qual pertence o direcionamento de zoom. |
| `*`zoomTargetHandle`*` | `xsd:string` | Sim | O identificador do destino de zoom a ser excluído. |

**Saída (deleteZoomTargetParam)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplo {#section-a35857a5ca884357a879f7ba6cf985fe}

Essa amostra de código exclui um direcionamento de zoom de uma empresa.

**Solicitação**

```java
<ns1:deleteZoomTargetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:zoomTargetHandle>34194|9|301</ns1:zoomTargetHandle>
</ns1:deleteZoomTargetParam>
```

**Resposta**

Nenhum.
