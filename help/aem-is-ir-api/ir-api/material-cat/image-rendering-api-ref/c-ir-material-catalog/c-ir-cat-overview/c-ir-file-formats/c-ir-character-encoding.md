---
description: A renderização de imagem suporta catálogos de materiais com codificação ISO-8859-1 e UTF-8.
seo-description: A renderização de imagem suporta catálogos de materiais com codificação ISO-8859-1 e UTF-8.
seo-title: Codificação de caracteres
solution: Experience Manager
title: Codificação de caracteres
topic: Dynamic Media Image Serving - Image Rendering API
uuid: efc3971b-dca1-4b47-a197-c10270ce17c9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# Codificação de caracteres{#character-encoding}

A renderização de imagem suporta catálogos de materiais com codificação ISO-8859-1 e UTF-8.

Uma marca de ordem de byte (BOM) é usada para especificar a codificação para cada arquivo. Para UTF-8, o BOM é a sequência de bytes `EF BB BF`. A codificação UTF-8 é assumida quando essa sequência de caracteres é detectada no início de cada arquivo de catálogo de materiais. Qualquer outra sequência de bytes resultará na interpretação do arquivo como sendo codificado para o padrão ISO-8859-1.

Muitos aplicativos contemporâneos, quando configurados para UTF-8, inserem a BOM automaticamente.
