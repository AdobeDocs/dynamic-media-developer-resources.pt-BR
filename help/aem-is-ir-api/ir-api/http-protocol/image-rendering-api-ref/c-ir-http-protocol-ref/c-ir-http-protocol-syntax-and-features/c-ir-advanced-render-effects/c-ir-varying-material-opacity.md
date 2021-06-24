---
description: A opacidade variável é suportada para texturas sólidas e repetíveis aplicadas a objetos sobrepostos, bem como para decalques e materiais de revestimento de janelas.
solution: Experience Manager
title: Opacidade variável dos materiais
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Opacidade variável dos materiais{#varying-material-opacity}

A opacidade variável é suportada para texturas sólidas e repetíveis aplicadas a objetos sobrepostos, bem como para decalques e materiais de revestimento de janelas.

As informações de opacidade podem ser fornecidas simplesmente usando uma imagem RGB com um canal alfa. Além disso, a opacidade geral pode ser variada com o comando `opacity=` (tanto para imagens RGB quanto RGBA).

Bordas de mural também suportam imagens RGBA, principalmente para suportar bordas recortadas.

Os arquivos [!DNL vnw] que definem os revestimentos de janela podem incluir um canal de opacidade, que é combinado pelo renderizador com o canal alfa da textura repetível e o valor `opacity=` para fornecer uma gama completa de efeitos de opacidade para tratamentos de janela simples e translúcidos.
