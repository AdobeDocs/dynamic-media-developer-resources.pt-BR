---
description: As camadas são posicionadas alinhando a origem da camada (origem=) com a origem da camada de fundo em um deslocamento especificado por pos=.
seo-description: As camadas são posicionadas alinhando a origem da camada (origem=) com a origem da camada de fundo em um deslocamento especificado por pos=.
seo-title: Inserção de camada
solution: Experience Manager
title: Inserção de camada
uuid: d9d778f2-13dd-4ea1-a703-52eac70bb3d8
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# Inserção de camada{#layer-placement}

As camadas são posicionadas alinhando a origem da camada (origem=) com a origem da camada de fundo em um deslocamento especificado por pos=.

Se a origem da camada não for especificada explicitamente para uma camada de imagem, ela será calculada da seguinte maneira:

1. Determine a âncora da imagem. Use `anchor=` ou, se não especificado, `catalog::Anchor`.
1. Se a âncora da imagem estiver definida, aplique as transformações de camada e `extend=` para convertê-la em um valor origin=.
1. Se nenhuma âncora de imagem for definida, a origem da camada será colocada no centro do retângulo da camada (após a aplicação de `extend=`).

![](assets/layerplacement.png)

