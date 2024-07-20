---
title: hei
description: Altura da imagem de resposta. Especifica o dimensionamento da imagem renderizada de forma que a altura da imagem de resposta não seja maior que o valor especificado, mantendo a proporção da imagem.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8e93aa32-b38e-46e4-be52-abd81222cfc3
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# hei{#hei}

Altura da imagem de resposta. Especifica o dimensionamento da imagem renderizada de forma que a altura da imagem de resposta não seja maior que o valor especificado, mantendo a proporção da imagem.

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>Altura da imagem de resposta em pixels (número inteiro maior que 0). </p></td> 
 </tr> 
</table>

A imagem não será preenchida se `wid=` e `hei=` forem especificados e a largura/altura for diferente da proporção da imagem.

`wid=` e `hei=` trabalham juntos para definir o tamanho da imagem retornada pelo servidor. Se `scl=` vier depois de `wid=` ou `hei=` na URL, ele cancelará esses comandos e `scl=` definirá o tamanho da imagem retornada pelo servidor.

No entanto, se `wid=` ou `hei=` vir depois de `scl=` na URL, eles cancelam `scl=` e `wid=`/ `hei=` definem o tamanho da imagem retornada pelo servidor.

>[!NOTE]
>
>Um erro será retornado se o tamanho da imagem de resposta calculada ou padrão for maior que `attribute::MaxPix`.

## Propriedades {#section-6cbc6acd37c847beab84c896ac25280c}

Pode ocorrer em qualquer lugar na solicitação. O redimensionamento da imagem com `wid=`, `hei=` ou `scl=` não altera o valor da resolução de impressão inserido na imagem de resposta. Ignorado se `scl=` ocorrer após `wid=` e/ou `hei=` na sequência de comandos.

## Padrão {#section-61043f6c1f5d450883ff9e5eafd95955}

Se `wid=`, `hei=` ou `scl=` não forem especificados, a imagem de resposta será dimensionada para se ajustar ao tamanho definido por `attribute::DefaultPix`. Se `attribute::DefaultPix` estiver vazio, a imagem de resposta terá o mesmo tamanho que a imagem de exibição da vinheta.

## Consulte também {#section-7ba51379f1e2421c92d3592d20a37734}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
