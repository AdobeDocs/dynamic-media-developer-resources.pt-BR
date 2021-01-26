---
description: Altura da imagem de resposta. Especifica o dimensionamento da imagem renderizada para que a altura da imagem de resposta não seja maior que o valor especificado, mantendo a proporção da imagem.
seo-description: Altura da imagem de resposta. Especifica o dimensionamento da imagem renderizada para que a altura da imagem de resposta não seja maior que o valor especificado, mantendo a proporção da imagem.
seo-title: hei
solution: Experience Manager
title: hei
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 616d3306-ccbd-4400-8a94-1ff6f47b802e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---


# hei{#hei}

Altura da imagem de resposta. Especifica o dimensionamento da imagem renderizada para que a altura da imagem de resposta não seja maior que o valor especificado, mantendo a proporção da imagem.

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>Responder altura da imagem em pixels (número inteiro maior que 0). </p></td> 
 </tr> 
</table>

A imagem não será preenchida se `wid=` e `hei=` forem especificados e a largura/altura for diferente da proporção da imagem.

`wid=` e  `hei=` trabalhe em conjunto para definir o tamanho da imagem que é retornada pelo servidor. Se `scl=` vier depois de `wid=` ou `hei=` no URL, ele cancelará esses comandos e `scl=` definirá o tamanho da imagem retornada pelo servidor.

No entanto, se `wid=` ou `hei=` vier depois de `scl=` no URL, eles cancelarão `scl=` e `wid=`/ `hei=` definirão o tamanho da imagem retornada pelo servidor.

>[!NOTE]
>
>Um erro será retornado se o tamanho da imagem de resposta calculada ou padrão for maior que `attribute::MaxPix`.

## Propriedades {#section-6cbc6acd37c847beab84c896ac25280c}

Pode ocorrer em qualquer lugar dentro da solicitação. Redimensionar a imagem com `wid=`, `hei=` ou `scl=` não altera o valor de resolução de impressão incorporado na imagem de resposta. Ignorado se `scl=` ocorrer depois de `wid=` e/ou `hei=` na sequência de comando.

## Padrão {#section-61043f6c1f5d450883ff9e5eafd95955}

Se `wid=`, `hei=` ou `scl=` não forem especificados, a imagem de resposta será dimensionada para se ajustar ao tamanho definido por `attribute::DefaultPix`. Se `attribute::DefaultPix` estiver vazio, a imagem de resposta terá o mesmo tamanho que a imagem de visualização da vinheta.

## Consulte também {#section-7ba51379f1e2421c92d3592d20a37734}

[atributo::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ,  [atributo::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29),  [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
