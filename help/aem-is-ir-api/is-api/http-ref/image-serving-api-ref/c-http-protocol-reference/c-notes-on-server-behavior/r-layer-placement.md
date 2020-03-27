---
description: As camadas são posicionadas alinhando a origem da camada (origem=) com a origem da camada de plano de fundo em um deslocamento especificado por pos=.
seo-description: As camadas são posicionadas alinhando a origem da camada (origem=) com a origem da camada de plano de fundo em um deslocamento especificado por pos=.
seo-title: Posicionamento da camada
solution: Experience Manager
title: Posicionamento da camada
topic: Scene7 Image Serving - Image Rendering API
uuid: d9d778f2-13dd-4ea1-a703-52eac70bb3d8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Posicionamento da camada{#layer-placement}

As camadas são posicionadas alinhando a origem da camada (origem=) com a origem da camada de plano de fundo em um deslocamento especificado por pos=.

Se a origem de camada não for especificada explicitamente para uma camada de imagem, ela será calculada da seguinte forma:

1. Determine a âncora da imagem. Use `anchor=`ou, se não for especificado, `catalog::Anchor`.
1. Se a âncora da imagem estiver definida, aplique as transformações da camada e converta- `extend=` a em um valor origem=.
1. Se nenhuma âncora de imagem estiver definida, a origem de camada será colocada no centro do retângulo de camada (após a aplicação `extend=`).

![](assets/layerplacement.png)

