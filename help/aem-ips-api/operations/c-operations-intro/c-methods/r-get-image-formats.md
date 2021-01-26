---
description: Retorna formatos de imagem, como PDF, EPS, SWF e outros.
seo-description: Retorna formatos de imagem, como PDF, EPS, SWF e outros.
seo-title: getImageFormats
solution: Experience Manager
title: getImageFormats
topic: Dynamic Media Image Production System API
uuid: 0adf989d-9c72-4337-99c0-de6931943e78
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---


# getImageFormats{#getimageformats}

Retorna formatos de imagem, como PDF, EPS, SWF e outros.

Sintaxe

## Tipos de usuário autorizados {#section-6a386ad8641b4aa1a281600fc94fd3f6}

* `IpsUser`
* `IspAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-eefa36a70b74498f8727ef61d98cfb63}

**Entrada (getImageFormatsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | A alça da empresa com os formatos de imagem que você deseja obter. |

**Saída (getImageFormatsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`imageFormatArray`*` | `types:ImageFormatArray` | Sim | A matriz de formato de imagem. |

## Exemplos {#section-73881e12839b4904bf3299b0920bdd0c}

Essa amostra de código retorna todos os formatos de imagem para a empresa especificada.

**Solicitação**

```java
<ns1:getImageFormatsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getImageFormatsParam>
```

**Resposta**

```java
<getImageFormatsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <imageFormatArray></imageFormatArray>
</getImageFormatsReturn>
```

