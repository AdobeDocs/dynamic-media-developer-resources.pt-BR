---
description: As transformações são aplicadas a imagens de origem e camadas de texto.
solution: Experience Manager
title: Transformações de camada
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5758d07c-bb84-4ab1-bf77-f59cf93f5e90
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# Transformações de camada{#layer-transforms}

As transformações são aplicadas a imagens de origem e camadas de texto.

As seguintes operações são aplicadas às imagens de origem, na ordem dada, para alcançar a relação espacial desejada com a camada 0:

1. Aplicar `crop=`, se especificado.
1. Escala com base em `size=` ou, se `size=` não for especificado, com base em `scale=`, ou, se `scale=` não for especificado, com base em `res=`, ou, se `res=` não for especificado, use a imagem de origem de resolução completa.
1. Aplicar `flip=`, se especificado.
1. Aplicar `rotate=`, se especificado.
1. Aplicar `extend=`, se especificado.
1. Posicione a camada na tela com base em `origin=` e `pos=` (veja abaixo).

As seguintes transformações são aplicadas às camadas de texto:

1. O tamanho da caixa de texto é determinado por `size=`, ou a largura e a altura do texto, se `size=` for apenas parcial ou não for fornecido. O texto é alinhado na caixa de texto usando os atributos de alinhamento de texto rtf. O texto pode ser cortado pela caixa de texto.
1. Dimensione o conteúdo de texto com base na resolução especificada com `textAttr=`.
1. Aplicar `rotate=`, se especificado.
1. Aplicar `extend=`, se especificado.
1. Posicione a camada na tela de desenho com base em `origin=` e `pos=` (veja abaixo).

Para camadas de imagem e texto, o último posicionamento da etapa na tela de desenho não se aplica à camada 0, já que a camada 0 constitui efetivamente a tela de desenho.
