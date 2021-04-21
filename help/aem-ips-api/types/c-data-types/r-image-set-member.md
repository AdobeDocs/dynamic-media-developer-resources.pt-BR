---
description: Ativos que pertencem a um conjunto de imagens.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---


# ImageSetMember{#imagesetmember}

Ativos que pertencem a um conjunto de imagens.

Redefinição de página significa que um [!DNL eCatalog] deve iniciar uma nova página. `RenderSet` indica que faz parte de uma  `RenderSet` amostra. O valor é forçado a `true` para `eCatalog` e `RenderSet` conjuntos.

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`ativo`*` | `type:Asset` | Ativos na matriz do conjunto de imagens. |
| `*`pageReset`*` | `xsd:boolean` | Inicia uma nova página. A configuração é ignorada e o valor é forçado a `true` para os conjuntos `eCatalog` e `RenderSet`. |

