---
description: Definição de público alvo para uma ação de clique no navegador.
seo-description: Definição de público alvo para uma ação de clique no navegador.
seo-title: ImageMapDefinition
solution: Experience Manager
title: ImageMapDefinition
topic: Dynamic Media Image Production System API
uuid: e3b9a304-5c43-46ce-8e87-860b49006a37
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 1%

---


# ImageMapDefinition{#imagemapdefinition}

Definição de público alvo para uma ação de clique no navegador.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`name`*` | `xsd:string` | O nome da definição do mapa de imagem. |
| `*`shapeType`*` | `xsd:string` | Um dos valores de forma de região. |
| `*`região`*` | `xsd:string` | Coordenadas do mapa de imagens. O formato é baseado nos atributos da tag HTML `<area>`. |
| `*`ação`*` | `xsd:string` | Outros atributos a serem incluídos na tag HTML `<area>`, incluindo o URL `href`. |
| `*`enabled`*` | `xsd:boolean` | True se o mapa de imagem estiver ativado. |

