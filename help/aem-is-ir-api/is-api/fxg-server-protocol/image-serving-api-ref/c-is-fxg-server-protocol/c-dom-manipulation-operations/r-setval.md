---
description: Defina o valor do nó de texto para s7 elementID.
seo-description: Defina o valor do nó de texto para s7 elementID.
seo-title: setVal
solution: Experience Manager
title: setVal
uuid: 27ced070-6434-477d-aacf-053d53ee58ff
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '75'
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
