---
description: Exclua qualquer atributo para uma determinada s7 elementID.
seo-description: Exclua qualquer atributo para uma determinada s7 elementID.
seo-title: deleteAttr
solution: Experience Manager
title: deleteAttr
uuid: b1176c1a-9ec3-4a95-9f91-97f9f168c252
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 0%

---


# deleteAttr{#deleteattr}

Exclua qualquer atributo para um determinado s7:elementID.

`deleteAttr.elementID={attributeName%26attributeName}`

Se um elemento de nó FXG tiver um `s7:elementID` definido, os atributos desse nó poderão ser excluídos com este comando.

## Exemplo {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

Este exemplo remove os atributos *[!DNL x]*, *[!DNL y]* e *[!DNL visible]* do nó FXG original.
