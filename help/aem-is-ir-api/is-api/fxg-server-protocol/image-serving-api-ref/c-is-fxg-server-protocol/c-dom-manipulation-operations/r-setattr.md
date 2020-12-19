---
description: Defina qualquer atributo para uma determinada s7 elementID.
seo-description: Defina qualquer atributo para uma determinada s7 elementID.
seo-title: setAttr
solution: Experience Manager
title: setAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: 968f7496-3cd4-4670-96fc-53127bba9a83
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---


# setAttr{#setattr}

Defina qualquer atributo para uma determinada s7:elementID.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

Se um elemento de nó FXG tiver `s7:elementID` definido, você poderá manipular os atributos desse nó. Você pode definir quantos pares de atributo/valor desejar. Os atributos não precisam ser definidos no FXG, mas devem ser válidos para o elemento node. Todos os valores entre `{}` devem ser Escapados.

## Exemplo {#section-9c37470d5f0349e5b0a97291782cb7a6}

Suponha que um atributo `s7:elementID="Group1"` esteja definido para um nó `BitmapGraphic`, o seguinte é válido:

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

Este exemplo define *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]* e *[!DNL scaleY]* para `BitmapGraphic` e substitui quaisquer valores existentes.
