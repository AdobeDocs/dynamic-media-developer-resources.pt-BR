---
description: Exclui um formato de imagem. Obtenha o identificador de formato de imagem de saveImageFormat.
solution: Experience Manager
title: deleteImageFormat
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: bd717c08-6da4-47f1-8614-e4ba79d8176c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '107'
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
| `*`imageFormatHandle`*` | `xsd:string` | Sim | O identificador para o formato de imagem que você deseja excluir. |

**Saída (deleteImageFormatParam)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-9ed9baaba13549bfaad1bc9cd7ec7009}

Essa amostra de código exclui um formato de imagem de uma empresa. Obtenha o identificador de formato de imagem de outra operação.

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
