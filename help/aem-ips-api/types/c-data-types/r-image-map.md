---
description: Público alvo para uma ação de clique no navegador.
seo-description: Público alvo para uma ação de clique no navegador.
seo-title: ImageMap
solution: Experience Manager
title: ImageMap
topic: Scene7 Image Production System API
uuid: 1a09ab27-7ee1-4162-8047-575f3f5ca8fe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---


# ImageMap{#imagemap}

Público alvo para uma ação de clique no navegador.

Sempre associado a uma imagem. Você pode obter um público alvo `ImageMap` de `ImageInfo`.

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| ` *`imageMapHandle`*` | `xsd:string` | Identificador do mapa de imagens. |
| ` *`name`*` | `xsd:string` | Nome do mapa de imagens. |
| ` *`região`*` | `xsd:string` | Coordenadas do mapa de imagens. O formato é baseado no atributo da tag HTML `<area>`. |
| ` *`ação`*` | `xsd:string` | Outros atributos a serem incluídos na tag HTML `<area>`, incluindo o URL `href`. |
| ` *`shapeType`*` | `xsd:boolean` | Um valor [!DNL RegionShape]. |
| ` *`position`*` | `xsd:string` | Posição no formato do atributo `<area>` do elemento HTML [!DNL coords]. Por exemplo: `coords ="0,0,84,128"`. |
| ` *`enabled`*` | `xsd:boolean` | True se o mapa de imagem estiver ativado. |
| ` *`lastModified`*` | `xsd:dateTime` | Data e hora em que o mapa de imagem foi modificado pela última vez. |

