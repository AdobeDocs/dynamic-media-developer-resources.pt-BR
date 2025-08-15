---
title: appendElement
description: Anexe XML a um elementID s7.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f93bc31e-c0ae-4375-bb6a-eba6f11945b2
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 0%

---

# appendElement{#appendelement}

Anexar XML a um s7:elementID.

`appendElement.elementID=<XML>`

Se um elemento do nó FXG tiver um `s7:elementID` definido, o valor `<XML>` será anexado como um elemento filho. O `<XML>` deve ser codificado.

## Exemplo {#section-4368570aa198485d91b73b4d0741478f}

Suponha que um atributo `s7:elementID="group1"` esteja definido para um nó Grupo, o seguinte será válido:

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

Este exemplo anexa um elemento gráfico de texto filho a `group1`.
