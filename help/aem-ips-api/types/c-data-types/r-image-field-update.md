---
description: Atualiza o campo de imagem associado a um ativo de imagem.
seo-description: Atualiza o campo de imagem associado a um ativo de imagem.
seo-title: ImageFieldUpdate
solution: Experience Manager
title: ImageFieldUpdate
topic: Scene7 Image Production System API
uuid: 0262be3e-f840-41cd-bedc-cc37d9982235
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---


# ImageFieldUpdate{#imagefieldupdate}

Atualiza o campo de imagem associado a um ativo de imagem.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Identificador de ativos. |
| ` *`resolução`*` | `xsd:double` | Resolução da imagem em pixels por polegada. |
| ` *`anchorX`*` | `xsd:int` | Âncora de imagem do eixo X. |
| ` *`anchorY`*` | `xsd:int` | Âncora de imagem do eixo Y. |
| ` *`userData`*` | `xsd:string` | Valor do campo de metadados `userData`, que é publicado no campo de catálogo de dados do usuário que serve a imagem. |

