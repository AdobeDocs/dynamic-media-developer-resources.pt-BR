---
description: Direcionamento para uma ação de clique no navegador.
solution: Experience Manager
title: ImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# [!DNL ImageMap]{#imagemap}

Direcionamento para uma ação de clique no navegador.

Sempre associado a uma imagem. Você pode obter um público alvo de `ImageMap` de `ImageInfo`.

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| imageMapHandle | `xsd:string` | Identificador do mapa de imagem. |
| [!DNL name] | `xsd:string` | Nome do mapa de imagem. |
| [!DNL region] | `xsd:string` | Coordenadas do mapa de imagem. O formato é baseado no atributo de tag HTML `<area>`. |
| [!DNL action] | `xsd:string` | Outros atributos a serem incluídos na tag HTML `<area>`, incluindo a URL `href`. |
| shapeType | `xsd:boolean` | Um valor [!DNL RegionShape]. |
| [!DNL position] | `xsd:string` | Posição no formato do atributo [!DNL coords] do elemento HTML `<area>`. Por exemplo: `coords ="0,0,84,128"`. |
| [!DNL enabled] | `xsd:boolean` | True se o mapa de imagem estiver habilitado. |
| lastModified | `xsd:dateTime` | Data e hora da última modificação do mapa de imagem. |
