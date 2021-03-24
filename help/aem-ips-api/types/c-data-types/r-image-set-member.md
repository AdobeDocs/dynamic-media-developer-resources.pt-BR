---
description: Ativos que pertencem a um conjunto de imagens.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic, SDK/API, Conjuntos de imagens
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
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

