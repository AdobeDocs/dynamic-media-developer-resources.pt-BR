---
description: Retorna formatos de imagem, como PDF, EPS, SWF e outros.
solution: Experience Manager
title: getImageFormato
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c2fa4cdd-fb4f-4e6a-8197-8f64c986c3a0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 0%

---

# getImageFormato{#getimageformats}

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
| companyHandle | `xsd:string` | Sim | O identificador da empresa com os formatos de imagem que você deseja obter. |

**Saída (getImageFormatsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| imageFormatArray | `types:ImageFormatArray` | Sim | A matriz de formato de imagem. |

## Exemplos {#section-73881e12839b4904bf3299b0920bdd0c}

Esta amostra de código retorna todos os formatos de imagem da empresa especificada.

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
