---
description: Direcione para uma ação de clique no navegador.
solution: Experience Manager
title: ImageMap
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '102'
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
