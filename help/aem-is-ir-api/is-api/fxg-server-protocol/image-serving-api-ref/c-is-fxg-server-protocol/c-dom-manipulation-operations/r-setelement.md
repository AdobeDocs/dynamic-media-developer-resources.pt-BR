---
description: Defina XML como um elementID s7.
solution: Experience Manager
title: setElement
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 979e6070-6e24-4caf-9d87-2c80b734c996
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 0%

---

# setElement{#setelement}

Defina XML como s7:elementID.

`setElement.elementID=<XML>`

Se um elemento de nó FXG tiver um `s7:elementID` definido, a variável `<XML>` é substituído como um elemento filho. A variável `<XML>` deve ser codificado.

## Exemplo {#section-f23a998b18994dd3b5d4e1965718db9f}

Assuma um `s7:elementID="group2"` o atributo é definido para um `Group` então o seguinte é válido:

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

Este exemplo remove todos os filhos do `group2`e o substitui por um novo `TextGraphic` nó filho.
