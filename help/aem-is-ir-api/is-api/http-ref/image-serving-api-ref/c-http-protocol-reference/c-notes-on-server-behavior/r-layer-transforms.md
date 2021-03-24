---
description: As transformações são aplicadas a imagens de origem e camadas de texto.
solution: Experience Manager
title: Transformações de camada
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---


# Transformações de camada{#layer-transforms}

As transformações são aplicadas a imagens de origem e camadas de texto.

As seguintes operações são aplicadas às imagens de origem, na ordem especificada, para alcançar o relacionamento espacial desejado com a camada 0:

1. Aplique `crop=`, se especificado.
1. Escala com base em `size=` ou, se `size=` não for especificado, com base em `scale=` ou, se `scale=` não for especificado, com base em `res=`, ou, se `res=` não for especificado, use a imagem de origem com resolução completa.
1. Aplique `flip=`, se especificado.
1. Aplique `rotate=`, se especificado.
1. Aplique `extend=`, se especificado.
1. Posicione a camada na tela com base em `origin=` e `pos=` (veja abaixo).

As seguintes transformações são aplicadas às camadas de texto:

1. O tamanho da caixa de texto é determinado por `size=`, ou a largura e altura do texto, se `size=` for apenas parcialmente ou não for fornecido. O texto é alinhado dentro da caixa de texto usando os atributos de alinhamento de texto rtf. O texto pode ser cortado pela caixa de texto.
1. Dimensione o conteúdo do texto com base na resolução especificada com `textAttr=`.
1. Aplique `rotate=`, se especificado.
1. Aplique `extend=`, se especificado.
1. Posicione a camada na tela com base em `origin=` e `pos=` (veja abaixo).

Para camadas de imagem e texto, o posicionamento da última etapa da camada na tela não se aplica à camada 0, pois a camada 0 constitui efetivamente a tela.
