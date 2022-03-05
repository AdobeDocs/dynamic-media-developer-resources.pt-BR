---
title: Opacidade variável dos materiais
description: A opacidade variável é suportada para texturas sólidas e repetíveis aplicadas a objetos sobrepostos, bem como para decalques e materiais de revestimento de janelas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Opacidade variável dos materiais{#varying-material-opacity}

A opacidade variável é suportada para texturas sólidas e repetíveis aplicadas a objetos sobrepostos, bem como para decalques e materiais de revestimento de janelas.

As informações de opacidade podem ser fornecidas simplesmente usando uma imagem RGB com um canal alfa. Além disso, a opacidade geral pode ser variada com a variável `opacity=` (para imagens RGB e RGBA).

Bordas de mural também suportam imagens RGBA, principalmente para suportar bordas recortadas.

O [!DNL vnw] os arquivos que definem coberturas de janela podem incluir um canal de opacidade. Ele é combinado pelo renderizador com o canal alfa da textura repetível e a variável `opacity=` para fornecer uma gama completa de efeitos de opacidade para tratamentos de janela simples e translúcidos.
