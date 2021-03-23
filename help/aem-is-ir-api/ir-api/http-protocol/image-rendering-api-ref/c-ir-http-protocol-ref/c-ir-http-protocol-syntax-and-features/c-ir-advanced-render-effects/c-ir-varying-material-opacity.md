---
description: A opacidade variável é suportada para texturas sólidas e repetíveis aplicadas a objetos sobrepostos, bem como para decalques e materiais de revestimento de janelas.
seo-description: A opacidade variável é suportada para texturas sólidas e repetíveis aplicadas a objetos sobrepostos, bem como para decalques e materiais de revestimento de janelas.
seo-title: Opacidade variável dos materiais
solution: Experience Manager
title: Opacidade variável dos materiais
uuid: 6af07ea8-44ba-4253-8a26-614725af2f46
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---


# Opacidade variável do material{#varying-material-opacity}

A opacidade variável é suportada para texturas sólidas e repetíveis aplicadas a objetos sobrepostos, bem como para decalques e materiais de revestimento de janelas.

As informações de opacidade podem ser fornecidas simplesmente usando uma imagem RGB com um canal alfa. Além disso, a opacidade geral pode ser variada com o comando `opacity=` (tanto para imagens RGB quanto RGBA).

Bordas de mural também suportam imagens RGBA, principalmente para suportar bordas recortadas.

Os arquivos [!DNL vnw] que definem os revestimentos de janela podem incluir um canal de opacidade, que é combinado pelo renderizador com o canal alfa da textura repetível e o valor `opacity=` para fornecer uma gama completa de efeitos de opacidade para tratamentos de janela simples e translúcidos.
