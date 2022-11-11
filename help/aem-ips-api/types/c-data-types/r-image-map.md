---
description: Direcione para uma ação de clique no navegador.
solution: Experience Manager
title: ImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 2%

---

# [!DNL ImageMap]{#imagemap}

Direcione para uma ação de clique no navegador.

Sempre associado a uma imagem. Você pode obter um `ImageMap` direcionar de `ImageInfo`.

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| imageMapHandle | `xsd:string` | Identificador do mapa de imagem. |
| [!DNL name] | `xsd:string` | Nome do mapa de imagem. |
| [!DNL region] | `xsd:string` | Coordenadas do mapa de imagem. O formato é baseado no HTML `<area>` atributo da tag . |
| [!DNL action] | `xsd:string` | Outros atributos a serem incluídos no HTML `<area>` , incluindo a `href` URL. |
| shapeType | `xsd:boolean` | A [!DNL RegionShape] valor. |
| [!DNL position] | `xsd:string` | Posição no formato do HTML `<area>` element&#39;s [!DNL coords] atributo. Por exemplo: `coords ="0,0,84,128"`. |
| [!DNL enabled] | `xsd:boolean` | Verdadeiro se o mapa de imagem estiver ativado. |
| lastModified | `xsd:dateTime` | Data e hora em que o mapa de imagem foi modificado pela última vez. |
