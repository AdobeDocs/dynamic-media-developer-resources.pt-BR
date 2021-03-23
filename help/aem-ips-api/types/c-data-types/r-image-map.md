---
description: Direcione para uma ação de clique no navegador.
seo-description: Direcione para uma ação de clique no navegador.
seo-title: ImageMap
solution: Experience Manager
title: ImageMap
uuid: 1a09ab27-7ee1-4162-8047-575f3f5ca8fe
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 3%

---


# ImageMap{#imagemap}

Direcione para uma ação de clique no navegador.

Sempre associado a uma imagem. Você pode obter um destino `ImageMap` de `ImageInfo`.

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`imageMapHandle`*` | `xsd:string` | Identificador do mapa de imagem. |
| `*`name`*` | `xsd:string` | Nome do mapa de imagem. |
| `*`região`*` | `xsd:string` | Coordenadas do mapa de imagem. O formato é baseado no atributo de tag HTML `<area>` . |
| `*`ação`*` | `xsd:string` | Outros atributos a serem incluídos na tag HTML `<area>` , incluindo a URL `href`. |
| `*`shapeType`*` | `xsd:boolean` | Um valor [!DNL RegionShape]. |
| `*`position`*` | `xsd:string` | Posição no formato do atributo `<area>` do elemento HTML [!DNL coords]. Por exemplo: `coords ="0,0,84,128"`. |
| `*`ativado`*` | `xsd:boolean` | Verdadeiro se o mapa de imagem estiver ativado. |
| `*`lastModified`*` | `xsd:dateTime` | Data e hora em que o mapa de imagem foi modificado pela última vez. |

