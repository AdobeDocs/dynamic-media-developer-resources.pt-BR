---
description: Retorna as coordenadas do quadrilateral que delimita o caminho nomeado do Photoshop.
solution: Experience Manager
title: getPhotoshopPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 46d88547-bb60-4370-9c79-bd281b40ba28
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# getPhotoshopPath{#getphotoshoppath}

Retorna as coordenadas do quadrilateral que delimita o caminho nomeado do Photoshop.

Sintaxe

## Tipos de usuário autorizados {#section-c417a287612847cb98dd0aa9c67fd78a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* &quot;

## Parâmetros {#section-ebffe496284c4ced9f329f78127be199}

**Entrada (getPhotoshopPathParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | Lide com a empresa com a imagem que deseja trabalhar. |
| assetHandle | `xsd:string` | Sim | Lide com o ativo de imagem. |
| pathName | `xsd:string` | Sim | Nome do caminho do Photoshop que você deseja retornar. |

**Saída (getPhotoshopPathReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| perspectivaQuad | `types:PerspectiveQuad` | Sim | Retorna as coordenadas da imagem com base no caminho. Consulte [PerspectivaQuad](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204). |

## Exemplos {#section-1f0461cbdc184c8d8925336d5279db47}

**Solicitação**

```java
<getPhotoshopPathParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <companyHandle>c|301</companyHandle>
  <assetHandle>a|26014</assetHandle>
  <pathName>Face Path</pathName>
</getPhotoshopPathParam>
```

**Resposta**

```java
<getPhotoshopPathReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <perspectiveQuad>
    <x0>932.19</x0>
    <y0>296.592</y0>
    <x1>968.769</x1>
    <y1>320.16</y1>
    <x2>1119.56</x2>
    <y2>1200.0</y2>
    <x3>900.43</x3>
    <y3>1200.0</y3>
  </perspectiveQuad>
</getPhotoshopPathReturn>
```

>[!MORELIKETHIS]
>
>* [PerspectivaQuad](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204)

