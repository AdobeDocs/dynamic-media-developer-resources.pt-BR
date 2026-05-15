---
description: Definição de direcionamento para uma ação de clique no navegador.
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
TQID: 'https://experienceleague.adobe.com/x27LpaNACQ5k-n09O-9Bhw7aecAjWQ6wNkLt8XewVXs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 71
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
