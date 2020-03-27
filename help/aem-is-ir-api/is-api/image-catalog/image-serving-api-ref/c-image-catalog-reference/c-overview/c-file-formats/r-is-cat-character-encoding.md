---
description: O Serviço de imagem suporta catálogos de imagem com codificação ISO-8859-1 e UTF-8.
seo-description: O Serviço de imagem suporta catálogos de imagem com codificação ISO-8859-1 e UTF-8.
seo-title: Codificação de caracteres
solution: Experience Manager
title: Codificação de caracteres
topic: Scene7 Image Serving - Image Rendering API
uuid: dfb56411-40d1-4bac-9213-9104ecba2a02
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Codificação de caracteres{#character-encoding}

O Serviço de imagem suporta catálogos de imagem com codificação ISO-8859-1 e UTF-8.

Uma marca de ordem de byte (BOM) é usada para especificar a codificação para cada arquivo. Para UTF-8, a BOM é a sequência de bytes `EF BB BF`. A codificação UTF-8 é assumida quando essa sequência de caracteres é detectada no início de cada arquivo de catálogo de imagens. Qualquer outra sequência de bytes resulta na interpretação do arquivo como sendo codificado para o padrão ISO-8859-1.

Muitos aplicativos contemporâneos, quando configurados para UTF-8, inserem a BOM automaticamente.
