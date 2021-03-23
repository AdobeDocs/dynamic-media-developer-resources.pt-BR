---
description: A renderização de imagem é compatível com catálogos de materiais com codificação ISO-8859-1 e UTF-8.
seo-description: A renderização de imagem é compatível com catálogos de materiais com codificação ISO-8859-1 e UTF-8.
seo-title: Codificação de caracteres
solution: Experience Manager
title: Codificação de caracteres
uuid: efc3971b-dca1-4b47-a197-c10270ce17c9
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# Codificação de caractere{#character-encoding}

A renderização de imagem é compatível com catálogos de materiais com codificação ISO-8859-1 e UTF-8.

Uma marca de ordem de byte (BOM) é usada para especificar a codificação para cada arquivo. Para UTF-8, a BOM é a sequência de bytes `EF BB BF`. A codificação UTF-8 é assumida quando essa sequência de caracteres é detectada no início de cada arquivo de catálogo de material. Qualquer outra sequência de bytes faz com que o arquivo seja interpretado como sendo codificado para o padrão ISO-8859-1.

Muitos aplicativos contemporâneos, quando configurados para UTF-8, inserem a BOM automaticamente.
