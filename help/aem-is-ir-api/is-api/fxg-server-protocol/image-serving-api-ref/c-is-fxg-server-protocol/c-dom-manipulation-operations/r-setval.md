---
description: Defina o valor do nó de texto para s7 elementID.
solution: Experience Manager
title: setVal
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---

# setVal{#setval}

Defina o valor do nó de texto para s7:elementID.

`setVal.elementID= *[!DNL value]*`

Se um elemento de nó FXG tiver um `s7:elementID` definido, o valor de texto desse nó poderá ser manipulado.

## Exemplo {#section-f574fd66dedd4a219aa537d7bdabea23}

Suponha que um atributo `s7:elementID="paragraph1"` esteja definido para um nó `TextGraphic`, o seguinte é válido:

`&setVal.paragraph=Hello`

Este exemplo define o valor de texto do nó de parágrafo como &quot;Hello&quot;.
