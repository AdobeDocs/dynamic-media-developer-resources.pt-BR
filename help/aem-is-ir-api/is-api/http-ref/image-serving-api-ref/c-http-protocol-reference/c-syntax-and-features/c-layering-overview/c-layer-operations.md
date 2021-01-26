---
description: Além das camadas de dimensionamento (size=) e posicionamento (pos=) relativas à camada 0 e que especificam a ordem de composição (a ordem z) com o comando layer=, as camadas podem ser giradas (rotate=) e viradas (flip=).
seo-description: Além das camadas de dimensionamento (size=) e posicionamento (pos=) relativas à camada 0 e que especificam a ordem de composição (a ordem z) com o comando layer=, as camadas podem ser giradas (rotate=) e viradas (flip=).
seo-title: Operações de camada
solution: Experience Manager
title: Operações de camada
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a9ef4199-cfa2-480e-a4de-8a0b9064a649
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# Operações de camada{#layer-operations}

Além das camadas de dimensionamento (size=) e posicionamento (pos=) relativas à camada 0 e que especificam a ordem de composição (a ordem z) com o comando layer=, as camadas podem ser giradas (rotate=) e viradas (flip=).

Os atributos `origin=` e `anchor=` podem ser usados para manter o alinhamento desejado entre as camadas quando imagens ou texto são alterados dinamicamente nos modelos.

O comando `maskUse=` está disponível para que as camadas de imagem acessem a área de plano de fundo das imagens que possuem máscaras separadas.

`opac=` pode ser usado para variar a opacidade da camada e  `hide=` para mostrar ou ocultar a camada.
