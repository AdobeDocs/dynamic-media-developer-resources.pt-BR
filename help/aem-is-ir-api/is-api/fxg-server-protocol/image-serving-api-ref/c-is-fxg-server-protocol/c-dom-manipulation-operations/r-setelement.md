---
description: Defina XML para um s7 elementID.
solution: Experience Manager
title: setElement
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '71'
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
