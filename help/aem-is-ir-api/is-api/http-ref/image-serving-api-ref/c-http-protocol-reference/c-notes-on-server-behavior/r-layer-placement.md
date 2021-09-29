---
title: Inserção de camada
escription: Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# Inserção de camada{#layer-placement}

As camadas são posicionadas alinhando a origem da camada (origem=) com a origem da camada de fundo em um deslocamento especificado por pos=.

Se a origem da camada não for especificada explicitamente para uma camada de imagem, ela será calculada da seguinte maneira:

1. Determine a âncora da imagem. Use `anchor=` ou, se não especificado, `catalog::Anchor`.
1. Se a âncora da imagem estiver definida, aplique as transformações de camada e `extend=` para convertê-la em um valor origin=.
1. Se nenhuma âncora de imagem for definida, a origem da camada será colocada no centro do retângulo da camada (após a aplicação de `extend=`).

![Imagem de posicionamento de camada](assets/layerplacement.png)
