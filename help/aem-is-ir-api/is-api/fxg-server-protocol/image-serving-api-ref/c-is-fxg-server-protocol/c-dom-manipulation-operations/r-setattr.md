---
description: Defina qualquer atributo para um determinado s7 elementID.
solution: Experience Manager
title: setAttr
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# setAttr{#setattr}

Defina qualquer atributo para um determinado s7:elementID.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

Se um elemento de nó FXG tiver um `s7:elementID` definido, você poderá manipular os atributos desse nó. Você pode definir quantos pares de atributo/valor desejar. Os atributos não precisam ser definidos no FXG, mas devem ser válidos para o elemento do nó. Todos os valores entre `{}` devem ser Escapados.

## Exemplo {#section-9c37470d5f0349e5b0a97291782cb7a6}

Suponha que um atributo `s7:elementID="Group1"` esteja definido para um nó `BitmapGraphic`, o seguinte é válido:

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

Este exemplo define *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]* e *[!DNL scaleY]* para `BitmapGraphic` e substitui quaisquer valores existentes.
