---
title: Codificação de caracteres
description: A Renderização de imagem suporta catálogos de materiais com codificação ISO-8859-1 e UTF-8.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ee7b33fd-7607-4bff-867b-6e7a837a9ed4
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# Codificação de caracteres{#character-encoding}

A Renderização de imagem suporta catálogos de materiais com codificação ISO-8859-1 e UTF-8.

Uma marca de ordem de byte (BOM) é usada para especificar a codificação de cada arquivo. Para UTF-8, a BOM é a sequência de bytes `EF BB BF`. A codificação UTF-8 é presumida quando esta sequência de caracteres é detectada no início de cada arquivo de catálogo de material. Qualquer outra sequência de bytes faz com que o arquivo seja interpretado como sendo codificado para o padrão ISO-8859-1.

Muitos aplicativos contemporâneos, quando configurados para UTF-8, inserem a BOM automaticamente.
