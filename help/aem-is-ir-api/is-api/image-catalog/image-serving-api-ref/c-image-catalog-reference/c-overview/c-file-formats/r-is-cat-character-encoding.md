---
description: O Image Serving suporta catálogos de imagens com codificação ISO-8859-1 e UTF-8.
solution: Experience Manager
title: Codificação de caracteres
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# Codificação de caractere{#character-encoding}

O Image Serving suporta catálogos de imagens com codificação ISO-8859-1 e UTF-8.

Uma marca de ordem de byte (BOM) é usada para especificar a codificação para cada arquivo. Para UTF-8, a BOM é a sequência de bytes `EF BB BF`. A codificação UTF-8 é assumida quando essa sequência de caracteres é detectada no início de cada arquivo de catálogo de imagem. Qualquer outra sequência de bytes resulta no arquivo ser interpretado como codificado no padrão ISO-8859-1.

Muitos aplicativos contemporâneos, quando configurados para UTF-8, inserem a BOM automaticamente.
