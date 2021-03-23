---
description: O Image Serving suporta catálogos de imagens com codificação ISO-8859-1 e UTF-8.
seo-description: O Image Serving suporta catálogos de imagens com codificação ISO-8859-1 e UTF-8.
seo-title: Codificação de caracteres
solution: Experience Manager
title: Codificação de caracteres
uuid: dfb56411-40d1-4bac-9213-9104ecba2a02
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# Codificação de caractere{#character-encoding}

O Image Serving suporta catálogos de imagens com codificação ISO-8859-1 e UTF-8.

Uma marca de ordem de byte (BOM) é usada para especificar a codificação para cada arquivo. Para UTF-8, a BOM é a sequência de bytes `EF BB BF`. A codificação UTF-8 é assumida quando essa sequência de caracteres é detectada no início de cada arquivo de catálogo de imagem. Qualquer outra sequência de bytes resulta no arquivo ser interpretado como codificado no padrão ISO-8859-1.

Muitos aplicativos contemporâneos, quando configurados para UTF-8, inserem a BOM automaticamente.
