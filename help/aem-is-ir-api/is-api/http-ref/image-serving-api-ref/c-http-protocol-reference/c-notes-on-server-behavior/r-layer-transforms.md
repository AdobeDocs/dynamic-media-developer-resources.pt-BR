---
description: As transformações são aplicadas a imagens de origem e camadas de texto.
seo-description: As transformações são aplicadas a imagens de origem e camadas de texto.
seo-title: Transformações de camada
solution: Experience Manager
title: Transformações de camada
topic: Scene7 Image Serving - Image Rendering API
uuid: b32b5af4-66ad-474a-9bca-4b6da8f43bf9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# Transformações de camada{#layer-transforms}

As transformações são aplicadas a imagens de origem e camadas de texto.

As seguintes operações são aplicadas às imagens de origem, na ordem especificada, para alcançar a relação espacial desejada com a camada 0:

1. Aplica `crop=`, se especificado.
1. Escala com base em `size=` ou, se `size=` não for especificado, com base em `scale=`, ou, se `scale=` não for especificado, com base em `res=`, ou, se `res=`não for especificado, use a imagem de origem de resolução completa.
1. Aplica `flip=`, se especificado.
1. Aplica `rotate=`, se especificado.
1. Aplica `extend=`, se especificado.
1. Posicione a camada na tela com base em `origin=` e `pos=` (veja abaixo).

As seguintes transformações são aplicadas às camadas de texto:

1. O tamanho da caixa de texto é determinado por `size=` ou pela largura e altura do texto, se `size=` for fornecido apenas parcialmente ou não for fornecido. O texto é alinhado dentro da caixa de texto usando os atributos de alinhamento de texto rtf. O texto pode ser cortado pela caixa de texto.
1. Dimensione o conteúdo do texto com base na resolução especificada com `textAttr=`.
1. Aplica `rotate=`, se especificado.
1. Aplica `extend=`, se especificado.
1. Posicione a camada na tela com base em `origin=` e `pos=` (veja abaixo).

Para camadas de imagem e texto, o posicionamento da última etapa na camada na tela não se aplica à camada 0, já que a camada 0 constitui efetivamente a tela.
