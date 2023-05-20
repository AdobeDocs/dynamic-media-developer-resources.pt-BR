---
title: Opacidade do material variável
description: A opacidade variável é suportada para cores sólidas e texturas repetíveis aplicadas a objetos sobrepostos, bem como para decalques e materiais de revestimento de janelas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Opacidade do material variável{#varying-material-opacity}

A opacidade variável é suportada para cores sólidas e texturas repetíveis aplicadas a objetos sobrepostos, bem como para decalques e materiais de revestimento de janelas.

As informações de opacidade podem ser fornecidas simplesmente usando uma imagem de RGB com um canal alfa. Além disso, a opacidade global pode ser `opacity=` (tanto para imagens RGB quanto RGBA).

Bordas de parede também suportam imagens RGBA, principalmente para suportar bordas cortadas por matriz.

A variável [!DNL vnw] os arquivos que definem revestimentos de janelas podem incluir um canal de opacidade. Ele é combinado pelo renderizador com o canal alfa da textura repetível e o `opacity=` valor para fornecer uma gama completa de efeitos de opacidade para tratamentos de janelas simples e translúcidas.
