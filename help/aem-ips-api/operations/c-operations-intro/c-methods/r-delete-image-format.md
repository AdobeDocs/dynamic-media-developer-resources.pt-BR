---
description: Exclui um formato de imagem. Obtenha o identificador de formato de imagem de saveImageFormat.
seo-description: Exclui um formato de imagem. Obtenha o identificador de formato de imagem de saveImageFormat.
seo-title: deleteImageFormat
solution: Experience Manager
title: deleteImageFormat
topic: Dynamic Media Image Production System API
uuid: 70dddde9-830b-4267-8ef5-df5241f549e3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---


# deleteImageFormat{#deleteimageformat}

Exclui um formato de imagem. Obtenha o identificador de formato de imagem de saveImageFormat.

Sintaxe

## Tipos de usuário autorizados {#section-827e24a3019543418b0a635d46c1edfd}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-462c05d9aad746ee8d2be0656041b693}

**Entrada (deleteImageFormatParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa que contém o formato de imagem que você deseja excluir. |
| `*`imageFormatHandle`*` | `xsd:string` | Sim | O identificador do formato de imagem que você deseja excluir. |

**Saída (deleteImageFormatParam)**

A API IPS não retorna uma resposta para esta operação.

## Exemplos {#section-9ed9baaba13549bfaad1bc9cd7ec7009}

Esta amostra de código exclui um formato de imagem de uma empresa. Obtenha o identificador de formato de imagem de outra operação.

**Solicitação**

```java
<deleteImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageFormatHandle>47|301</imageFormatHandle>
</deleteImageFormatParam>
```

**Resposta**

Nenhum.

**Tópico relacionado:**

[saveImageFormat](../../../operations/c-operations-intro/c-methods/r-save-image-format.md#reference-d15c27f533ef41e38b54a539a304bd1d)
