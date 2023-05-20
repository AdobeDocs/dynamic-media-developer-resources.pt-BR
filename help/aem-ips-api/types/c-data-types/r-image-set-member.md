---
description: Ativos que pertencem a um conjunto de imagens.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 0%

---

# [!DNL ImageSetMember]{#imagesetmember}

Ativos que pertencem a um conjunto de imagens.

A redefinição de página significa que um [!DNL eCatalog] A deve iniciar uma nova página. `RenderSet` indica que faz parte de um `RenderSet` amostra. O valor é forçado a `true` para `eCatalog` e `RenderSet` conjuntos.

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| ativo | `type:Asset` | Ativos na matriz do conjunto de imagens. |
| pageReset | `xsd:boolean` | Inicia uma nova página. A configuração é ignorada e o valor é forçado a `true` para `eCatalog` e `RenderSet` conjuntos. |
