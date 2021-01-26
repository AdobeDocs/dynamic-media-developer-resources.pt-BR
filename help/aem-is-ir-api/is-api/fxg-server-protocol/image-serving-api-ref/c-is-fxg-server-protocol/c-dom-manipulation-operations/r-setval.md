---
description: Defina o valor do nó de texto para s7 elementID.
seo-description: Defina o valor do nó de texto para s7 elementID.
seo-title: setVal
solution: Experience Manager
title: setVal
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 27ced070-6434-477d-aacf-053d53ee58ff
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

---


# setVal{#setval}

Defina o valor do nó de texto para s7:elementID.

`setVal.elementID= *[!DNL value]*`

Se um elemento de nó FXG tiver `s7:elementID` definido, o valor de texto desse nó poderá ser manipulado.

## Exemplo {#section-f574fd66dedd4a219aa537d7bdabea23}

Suponha que um atributo `s7:elementID="paragraph1"` esteja definido para um nó `TextGraphic`, o seguinte é válido:

`&setVal.paragraph=Hello`

Este exemplo define o valor de texto para o nó de parágrafo como &quot;Hello&quot;.
