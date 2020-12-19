---
description: Defina os atributos como elemento raiz FXG.
seo-description: Defina os atributos como elemento raiz FXG.
seo-title: setAttr.rootElement
solution: Experience Manager
title: setAttr.rootElement
topic: Scene7 Image Serving - Image Rendering API
uuid: dda16612-57c7-4abe-8aa4-00e599a8ea69
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 0%

---


# setAttr.rootElement{#setattr-rootelement}

Defina os atributos como elemento raiz FXG.

` setAttr.rootElement={ *[!DNL attributeName]*= *[!DNL attributeValue]*%26 *[!DNL attributeName]*= *[!DNL attributeValue]*}`

Esse comando pode manipular atributos do elemento raiz.

## Exemplo {#section-2758a6e316c34b99b13b02147e5973bb}

Se tivermos o seguinte elemento raiz:

`<Graphic version="1.0" viewHeight="692" viewWidth="792" s7:appVersion="1.0.0.11" ai:appVersion="14.0.0.367" d:id="1" xmlns="http://ns.adobe.com/fxg/2008" xmlns:ai="http://ns.adobe.com/ai/2008" xmlns:d="http://ns.adobe.com/fxg/2008/dt" xmlns:s7="http://ns.adobe.com/S7FXG/2008">`

Após aplicar o seguinte comando:

`setAttr.rootElement={viewHeight=300%26viewWidth=200}`

O elemento raiz agora é alterado para o seguinte:

`<Graphic xmlns="http://ns.adobe.com/fxg/2008" xmlns:ai="http://ns.adobe.com/ai/2008" xmlns:d="http://ns.adobe.com/fxg/2008/dt" xmlns:s7="http://ns.adobe.com/S7FXG/2008" ai:appVersion="14.0.0.367" d:id="1" s7:appVersion="1.0.0.11" version="1.0" viewHeight="300" viewWidth="200">`
