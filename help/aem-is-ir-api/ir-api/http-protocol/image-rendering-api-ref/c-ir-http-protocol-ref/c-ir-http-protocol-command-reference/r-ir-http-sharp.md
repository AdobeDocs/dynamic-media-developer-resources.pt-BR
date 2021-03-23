---
description: Textura nítida. Especifica a nitidez a ser aplicada ao renderizar este material.
seo-description: Textura nítida. Especifica a nitidez a ser aplicada ao renderizar este material.
seo-title: nítido
solution: Experience Manager
title: nítido
uuid: 8265eebf-9cec-4ad3-8b22-0f46f33a89f1
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 2%

---


# nítido{#sharp}

Textura nítida. Especifica a nitidez a ser aplicada ao renderizar este material.

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Sem nitidez. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Nitidez normal (tardia). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0 nitidez alternativa (início). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Mais nitidez (inicial e final). </p> </td> 
 </tr> 
</table>

`sharp=1` Aplica a nitidez após a transformação do material;  `sharp=2` Aplica a nitidez após a escala inicial da textura, mas antes de a transformar em cena;  `sharp=3` aplica a nitidez antes e depois da transformação.

O algoritmo de nitidez e a quantidade de nitidez e outros parâmetros USM (máscara com nitidez) são controlados pelo modelo de material padrão fornecido pela vinheta ou com `rs=`.

## Propriedades {#section-498ec9fcb8eb415fb99532d36c11d4c7}

Atributo de material. Ignorado por materiais de cor sólida.

## Padrão {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`, se o material for baseado em uma entrada de catálogo, caso contrário  `attribute::Sharp`.

## Consulte também {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[catálogo::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) ,  [sharpen=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e),  [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)
