---
description: A opacidade variável é suportada para texturas de cor sólida e repetitivas aplicadas a objetos sobrepostos, bem como para decalques e materiais de revestimento de janelas.
seo-description: A opacidade variável é suportada para texturas de cor sólida e repetitivas aplicadas a objetos sobrepostos, bem como para decalques e materiais de revestimento de janelas.
seo-title: Opacidade variável dos materiais
solution: Experience Manager
title: Opacidade variável dos materiais
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6af07ea8-44ba-4253-8a26-614725af2f46
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# Opacidade variável de material{#varying-material-opacity}

A opacidade variável é suportada para texturas de cor sólida e repetitivas aplicadas a objetos sobrepostos, bem como para decalques e materiais de revestimento de janelas.

As informações de opacidade podem ser fornecidas simplesmente usando uma imagem RGB com um canal alfa. Além disso, a opacidade geral pode variar com o comando `opacity=` (tanto para imagens RGB quanto RGBA).

As bordas de mural também suportam imagens RGBA, principalmente para suportar bordas cortadas.

Os arquivos [!DNL vnw] que definem as coberturas de janela podem incluir um canal de opacidade, que é combinado pelo renderizador com o canal alfa da textura repetível e o valor `opacity=` para fornecer uma gama completa de efeitos de opacidade para tratamentos de janela simples e translúcidos.
