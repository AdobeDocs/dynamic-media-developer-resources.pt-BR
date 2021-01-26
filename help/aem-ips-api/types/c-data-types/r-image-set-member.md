---
description: Ativos que pertencem a um conjunto de imagens.
seo-description: Ativos que pertencem a um conjunto de imagens.
seo-title: ImageSetMember
solution: Experience Manager
title: ImageSetMember
topic: Dynamic Media Image Production System API
uuid: bd013609-aed7-4c85-80f9-16be7fce99a3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---


# ImageSetMember{#imagesetmember}

Ativos que pertencem a um conjunto de imagens.

Redefinição de página significa que um [!DNL eCatalog] deve start uma nova página. `RenderSet` indica que faz parte de uma  `RenderSet` amostra. O valor é forçado a `true` para os conjuntos `eCatalog` e `RenderSet`.

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`ativo`*` | `type:Asset` | Ativos na matriz do conjunto de imagens. |
| `*`pageReset`*` | `xsd:boolean` | Start uma nova página. A configuração é ignorada e o valor é forçado a `true` para `eCatalog` e `RenderSet` conjuntos. |

