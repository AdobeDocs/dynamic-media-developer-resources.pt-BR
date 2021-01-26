---
description: Modo de reamostragem. Seleciona o algoritmo de reamostragem e/ou interpolação a ser usado para dimensionar a imagem renderizada para o tamanho especificado com wid=, hei= ou scl=.
seo-description: Modo de reamostragem. Seleciona o algoritmo de reamostragem e/ou interpolação a ser usado para dimensionar a imagem renderizada para o tamanho especificado com wid=, hei= ou scl=.
seo-title: resMode
solution: Experience Manager
title: resMode
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 106da74a-d7da-4998-a719-c4c69ae36f6b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---


# resMode{#resmode}

Modo de reamostragem. Seleciona o algoritmo de reamostragem e/ou interpolação a ser usado para dimensionar a imagem renderizada para o tamanho especificado com wid=, hei= ou scl=.

` `resMode=bilin|bicub|shar2|bisharp&quot;

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bilhão  </span> </p> </td> 
   <td colname="col2"> <p>Seleciona a interpolação bilinear padrão. Método de reamostragem mais rápido; alguns artefatos de aliasing podem ser perceptíveis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bicub  </span> </p> </td> 
   <td colname="col2"> <p>Seleciona a interpolação bicúbica. Mais intensiva em CPU do que a interpolação bilinear, mas produzirá imagens mais nítidas com artefatos de aliasing menos perceptíveis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> aguda2  </span> </p> </td> 
   <td colname="col2"> <p>Seleciona uma função Lanczos Window modificada como um algoritmo de interpolação. Pode produzir resultados ligeiramente mais nítidos do que bicúbicos a um custo de CPU mais alto. </p> <p> <span class="codeph"> O afiado  </span> foi substituído pelo  <span class="codeph"> afiado2  </span>, que tem uma probabilidade menor de causar artefatos aliasados, também conhecido como Moiré. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharp  </span> </p> </td> 
   <td colname="col2"> <p>Seleciona o resamplador padrão <span class="keyword"> Adobe Photoshop </span> para reduzir o tamanho da imagem, que é chamado de "divisor bicúbico" em <span class="keyword"> Adobe Photoshop </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-ea7029f37e094d9cb85646b85fbac0ce}

Pode ocorrer em qualquer lugar dentro da solicitação. Ignorado se nenhuma escala de imagem final for aplicada.

## Padrão {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## Consulte também {#section-16c557a2250e4f04b3e6cbef18add9ce}

[atributo::ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) ,  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
