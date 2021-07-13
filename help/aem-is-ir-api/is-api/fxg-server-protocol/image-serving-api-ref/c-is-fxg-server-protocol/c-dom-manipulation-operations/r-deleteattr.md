---
description: Exclua qualquer atributo para uma determinada s7 elementID.
solution: Experience Manager
title: deleteAttr
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 7cecd0aa-c928-4652-a92f-f21ebcf83304
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '54'
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
