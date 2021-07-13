---
description: O Image Serving suporta catálogos de imagens com codificação ISO-8859-1 e UTF-8.
solution: Experience Manager
title: Codificação de caracteres
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: e6e50c2a-53d3-4776-a3f6-4a9d3407e562
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# Codificação de caracteres{#character-encoding}

O Image Serving suporta catálogos de imagens com codificação ISO-8859-1 e UTF-8.

Uma marca de ordem de byte (BOM) é usada para especificar a codificação para cada arquivo. Para UTF-8, a BOM é a sequência de bytes `EF BB BF`. A codificação UTF-8 é assumida quando essa sequência de caracteres é detectada no início de cada arquivo de catálogo de imagem. Qualquer outra sequência de bytes resulta no arquivo ser interpretado como codificado no padrão ISO-8859-1.

Muitos aplicativos contemporâneos, quando configurados para UTF-8, inserem a BOM automaticamente.
