---
title: setAttr
description: Defina qualquer atributo para um elementID s7 específico.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# setAttr{#setattr}

Defina qualquer atributo para um determinado s7:elementID.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

Se um elemento de nó FXG tiver um `s7:elementID` definido, você poderá manipular os atributos desse nó. Você pode definir quantos pares de atributo/valor desejar. Os atributos não precisam estar já definidos no FXG, mas devem ser válidos para o elemento de nó. Todos os valores entre `{}` devem ser Escaped.

## Exemplo {#section-9c37470d5f0349e5b0a97291782cb7a6}

Suponha que um atributo `s7:elementID="Group1"` esteja definido para um nó `BitmapGraphic`, então o seguinte é válido:

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

Este exemplo define *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]* e *[!DNL scaleY]* para `BitmapGraphic` e substitui quaisquer valores existentes.
