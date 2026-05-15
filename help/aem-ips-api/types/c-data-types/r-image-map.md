---
description: Direcionamento para uma ação de clique no navegador.
solution: Experience Manager
title: ImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
TQID: 'https://experienceleague.adobe.com/ikMxCQ23L0HzbfmRlcYGL-fRJFK2uhwbZHNzcy1c25k'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 91
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
| [!DNL region] | `xsd:string` | Coordenadas do mapa de imagem. O formato é baseado no atributo de marca HTML `<area>`. |
| [!DNL action] | `xsd:string` | Outros atributos a serem incluídos na marca `<area>` do HTML, incluindo a URL `href`. |
| shapeType | `xsd:boolean` | Um valor [!DNL RegionShape]. |
| [!DNL position] | `xsd:string` | Posição no formato do atributo [!DNL coords] do elemento `<area>` do HTML. Por exemplo: `coords ="0,0,84,128"`. |
| [!DNL enabled] | `xsd:boolean` | True se o mapa de imagem estiver habilitado. |
| lastModified | `xsd:dateTime` | Data e hora da última modificação do mapa de imagem. |
