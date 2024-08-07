---
title: sharp
description: Nitidez da textura. Especifica a nitidez a ser aplicada na renderização deste material.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7921ceba-e249-4aab-823e-c54705c4a7c3
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# sharp{#sharp}

Nitidez da textura. Especifica a nitidez a ser aplicada na renderização deste material.

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Sem nitidez. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Nitidez normal (tardia). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0 nitidez alternativa (antecipada). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Mais nitidez (precoce e tardia). </p> </td> 
 </tr> 
</table>

`sharp=1` Aplica nitidez depois que o material é renderizado; `sharp=2` aplica nitidez após o dimensionamento inicial da textura, mas antes de ser transformada em cena; `sharp=3` aplica nitidez antes e depois da transformação.

O algoritmo de nitidez e a quantidade de nitidez e outros parâmetros USM (unsharp masking) são controlados pelo modelo de material padrão fornecido pela vinheta ou com `rs=`.

## Propriedades {#section-498ec9fcb8eb415fb99532d36c11d4c7}

Atributo de material. Ignorado por materiais de cores sólidas.

## Padrão {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`, se o material for baseado em uma entrada de catálogo, caso contrário `attribute::Sharp`.

## Consulte também {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[catálogo::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) , [sharpen=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e), [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)
