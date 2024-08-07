---
title: resMode
description: Modo de reamostragem. Seleciona o algoritmo de reamostragem e/ou interpolação a ser usado para dimensionar a imagem renderizada para o tamanho especificado com wid=, hei= ou scl=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0926dcfe-881c-4b52-b08d-c56afa0ba04d
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---

# resMode{#resmode}

Modo de reamostragem. Seleciona o algoritmo de reamostragem e/ou interpolação a ser usado para dimensionar a imagem renderizada para o tamanho especificado com `wid=`, `hei=` ou `scl=`.

` `resMode=bilin|bicub|sharp2|bisharp&quot;

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bilhão </span> </p> </td> 
   <td colname="col2"> <p>Seleciona a interpolação bilinear padrão. Método de reamostragem mais rápido; alguns artefatos de suavização podem ser visíveis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>Seleciona a interpolação bicúbica. Mais uso intenso da CPU do que a interpolação bilinear, mas produz imagens mais nítidas com menos artefatos de suavização visíveis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>Seleciona uma função de janela Lanczos modificada como um algoritmo de interpolação. Pode produzir resultados ligeiramente mais nítidos do que bicúbico a um custo de CPU mais alto. </p> <p> <span class="codeph"> sharp </span> foi substituído por <span class="codeph"> sharp2 </span>, que tem uma probabilidade menor de causar artefatos de suavização, também conhecido como Moiré. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharp </span> </p> </td> 
   <td colname="col2"> <p>Seleciona o reamostragem padrão <span class="keyword"> do Adobe Photoshop </span> para redução do tamanho da imagem, o qual é chamado de "nitidez bicúbica" no <span class="keyword"> Adobe Photoshop </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-ea7029f37e094d9cb85646b85fbac0ce}

Pode ocorrer em qualquer lugar na solicitação. Ignorado se nenhuma escala de imagem final for aplicada.

## Padrão {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## Consulte também {#section-16c557a2250e4f04b3e6cbef18add9ce}

[attribute::ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
