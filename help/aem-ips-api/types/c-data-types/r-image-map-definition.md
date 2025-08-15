---
description: Definição de direcionamento para uma ação de clique no navegador.
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---

# [!DNL ImageMapDefinition]{#imagemapdefinition}

Definição de direcionamento para uma ação de clique no navegador.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| name | `xsd:string` | O nome da definição do mapa de imagem. |
| shapeType | `xsd:string` | Um dos valores de shape de região. |
| região | `xsd:string` | Coordenadas do mapa de imagem. O formato é baseado nos atributos de tag `<area>` da HTML. |
| ação | `xsd:string` | Outros atributos a serem incluídos na marca `<area>` do HTML, incluindo a URL `href`. |
| habilitado | `xsd:boolean` | True se o mapa de imagem estiver habilitado. |
