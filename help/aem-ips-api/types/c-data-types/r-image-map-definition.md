---
description: Definição de meta para uma ação de clique no navegador.
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 1%

---


# ImageMapDefinition{#imagemapdefinition}

Definição de meta para uma ação de clique no navegador.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`name`*` | `xsd:string` | O nome da definição do mapa de imagem. |
| `*`shapeType`*` | `xsd:string` | Um dos valores de forma de região. |
| `*`região`*` | `xsd:string` | Coordenadas do mapa de imagem. O formato é baseado nos atributos de tag HTML `<area>` . |
| `*`ação`*` | `xsd:string` | Outros atributos a serem incluídos na tag HTML `<area>` , incluindo a URL `href`. |
| `*`ativado`*` | `xsd:boolean` | Verdadeiro se o mapa de imagem estiver ativado. |

