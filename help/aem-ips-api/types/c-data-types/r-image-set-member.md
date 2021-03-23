---
description: Ativos que pertencem a um conjunto de imagens.
seo-description: Ativos que pertencem a um conjunto de imagens.
seo-title: ImageSetMember
solution: Experience Manager
title: ImageSetMember
uuid: bd013609-aed7-4c85-80f9-16be7fce99a3
feature: Dynamic Media Classic, SDK/API, Conjuntos de imagens
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '86'
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

