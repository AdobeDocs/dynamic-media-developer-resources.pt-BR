---
description: Defina XML antes ou depois de um nó.
solution: Experience Manager
title: insertBefore,insertAfter
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 20d27fa7-e98a-4f85-9e48-5fa9ad3102b7
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 0%

---

# insertBefore,insertAfter{#insertbefore-insertafter}

Defina XML antes ou depois de um nó.

`insertBefore=<xml>, insertAfter=<xml>`

Se um elemento de nó FXG tiver um `s7:elementID` definido, podemos adicionar fragmentos XML antes ou depois desse nó com esse comando.

## Exemplo {#section-1fc8d4135ef94b60b838391e1568e70e}

Se houver uma tag de Grupo como esta:

`<Group visible="true" s7:elementID="inner_shape">`

em seguida:

`insertBefore.inner_shape=<Rect x="74.354" y="182.762" width="75" height="75" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" rotation="0"><fill><SolidColor color="%23ffffff" s7:cmykColor="%2300000000"/></fill></Rect>`

resulta em:

`<Rect height="75" rotation="0" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" width="75" x="74.354" y="182.762"><fill><SolidColor color="#ffffff" s7:cmykColor="#00000000"/></fill></Rect><Group s7:elementID="inner_shape" visible="true">`

`insertAfter.inner_shape=<Rect x="74.354" y="182.762" width="75" height="75" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" rotation="0"><fill><SolidColor color="%23ffffff" s7:cmykColor="%2300000000"/></fill></Rect>`

resulta em:

`<Group s7:elementID="inner_shape" visible="true"> <Rect ai:knockout="0" d:userLabel="Background" height="392.581" visible="true" width="319.953" x="0.75" y="0.75"> <fill><SolidColor color="#ffffff" s7:cmykColor="#00000000"/></fill> </Rect>`
