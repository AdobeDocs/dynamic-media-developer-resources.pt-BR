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

---


# ImageMap{#imagemap}

Público alvo para uma ação de clique no navegador.

Sempre associado a uma imagem. Você pode tirar um `ImageMap` público alvo de `ImageInfo`.

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| ` *`imageMapHandle`*` | `xsd:string` | Identificador do mapa de imagens. |
| ` *`name`*` | `xsd:string` | Nome do mapa de imagens. |
| ` *`região`*` | `xsd:string` | Coordenadas do mapa de imagens. O formato é baseado no atributo da `<area>` tag HTML. |
| ` *`ação`*` | `xsd:string` | Outros atributos a serem incluídos na `<area>` tag HTML, incluindo o `href` URL. |
| ` *`shapeType`*` | `xsd:boolean` | Um [!DNL RegionShape] valor. |
| ` *`posição`*` | `xsd:string` | Posição no formato do atributo do `<area>` elemento HTML [!DNL coords] . Por exemplo: `coords ="0,0,84,128"`. |
| ` *`enabled`*` | `xsd:boolean` | True se o mapa de imagem estiver ativado. |
| ` *`lastModified`*` | `xsd:dateTime` | Data e hora em que o mapa de imagem foi modificado pela última vez. |

