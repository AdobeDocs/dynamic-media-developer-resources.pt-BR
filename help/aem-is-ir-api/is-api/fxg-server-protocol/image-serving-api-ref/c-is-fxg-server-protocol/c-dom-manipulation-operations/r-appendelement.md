---
description: Anexar XML a uma s7 elementID.
seo-description: Anexar XML a uma s7 elementID.
seo-title: appendElement
solution: Experience Manager
title: appendElement
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 062c8288-4517-42a1-9f9f-f3c7bbb4b63b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---


# appendElement{#appendelement}

Anexar XML a um s7:elementID.

`appendElement.elementID=<XML>`

Se um elemento de nó FXG tiver um `s7:elementID` definido, o valor `<XML>` será anexado como um elemento filho. O `<XML>` deve ser codificado.

## Exemplo {#section-4368570aa198485d91b73b4d0741478f}

Suponha que um atributo `s7:elementID="group1"` esteja definido para um nó Grupo, o seguinte é válido:

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

Este exemplo anexa um filho gráfico de texto a `group1`.
