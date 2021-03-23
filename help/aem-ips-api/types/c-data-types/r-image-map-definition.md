---
description: Definição de meta para uma ação de clique no navegador.
seo-description: Definição de meta para uma ação de clique no navegador.
seo-title: ImageMapDefinition
solution: Experience Manager
title: ImageMapDefinition
uuid: e3b9a304-5c43-46ce-8e87-860b49006a37
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '89'
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

