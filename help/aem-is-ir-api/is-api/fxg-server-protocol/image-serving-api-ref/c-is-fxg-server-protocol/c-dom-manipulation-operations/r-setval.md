---
title: setVal
description: Defina o valor do nó de texto para s7 elementID.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 0%

---

# setVal{#setval}

Defina o valor do nó de texto para s7:elementID.

`setVal.elementID= *[!DNL value]*`

Se um elemento de nó FXG tiver uma `s7:elementID` definido, o valor de texto desse nó poderá ser manipulado.

## Exemplo {#section-f574fd66dedd4a219aa537d7bdabea23}

Assuma um `s7:elementID="paragraph1"` o atributo é definido para um `TextGraphic` então o seguinte é válido:

`&setVal.paragraph=Hello`

Este exemplo define o valor do texto do nó do parágrafo como &quot;Olá&quot;.
