---
description: Defina XML como s7 elementID.
seo-description: Defina XML como s7 elementID.
seo-title: setElement
solution: Experience Manager
title: setElement
topic: Scene7 Image Serving - Image Rendering API
uuid: 717c9c3c-a2e0-4179-8158-9913f4e09a96
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setElement{#setelement}

Defina XML como s7:elementID.

`setElement.elementID=<XML>`

Se um elemento de nó FXG tiver um `s7:elementID` definido, o `<XML>` valor será substituído como um elemento filho. The `<XML>` must be encoded.

## Example {#section-f23a998b18994dd3b5d4e1965718db9f}

Suponha que um `s7:elementID="group2"` atributo esteja definido para um `Group` nó, o seguinte é válido:

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

Este exemplo remove todos os filhos do `group2`nó e o substitui pelo novo nó `TextGraphic` filho.
