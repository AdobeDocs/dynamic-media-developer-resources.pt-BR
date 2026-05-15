---
title: Opacidade do material variável
description: A opacidade variável é suportada para cores sólidas e texturas repetíveis aplicadas a objetos sobrepostos, bem como para decalques e materiais de revestimento de janelas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
TQID: 'https://experienceleague.adobe.com/i4d6vy62vn9BfFrS2W0srO671N9Ad4hCUXR7J4cajJA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 138
ht-degree: 0%

---

# Opacidade do material variável{#varying-material-opacity}

A opacidade variável é suportada para cores sólidas e texturas repetíveis aplicadas a objetos sobrepostos, bem como para decalques e materiais de revestimento de janelas.

As informações de opacidade podem ser fornecidas simplesmente usando uma imagem do RGB com um canal alfa. Além disso, a opacidade geral pode variar com o comando `opacity=` (tanto para imagens RGB quanto RGBA).

Bordas de parede também suportam imagens RGBA, principalmente para suportar bordas cortadas por matriz.

Os arquivos [!DNL vnw] que definem coberturas de janelas podem incluir um canal de opacidade. Ele é combinado pelo renderizador com o canal alfa da textura repetível e o valor `opacity=` para fornecer uma gama completa de efeitos de opacidade para tratamentos de janelas simples e translúcidas.
