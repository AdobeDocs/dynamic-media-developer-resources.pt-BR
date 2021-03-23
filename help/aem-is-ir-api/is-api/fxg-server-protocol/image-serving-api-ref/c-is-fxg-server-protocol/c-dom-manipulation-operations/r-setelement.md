---
description: Defina XML para um s7 elementID.
seo-description: Defina XML para um s7 elementID.
seo-title: setElement
solution: Experience Manager
title: setElement
uuid: 717c9c3c-a2e0-4179-8158-9913f4e09a96
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---


# setElement{#setelement}

Defina XML como s7:elementID.

`setElement.elementID=<XML>`

Se um elemento de nó FXG tiver um `s7:elementID` definido, o valor `<XML>` será substituído como um elemento filho. O `<XML>` deve ser codificado.

## Exemplo {#section-f23a998b18994dd3b5d4e1965718db9f}

Suponha que um atributo `s7:elementID="group2"` esteja definido para um nó `Group`, o seguinte é válido:

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

Este exemplo remove todos os filhos do nó `group2`e o substitui pelo novo nó filho `TextGraphic`.
