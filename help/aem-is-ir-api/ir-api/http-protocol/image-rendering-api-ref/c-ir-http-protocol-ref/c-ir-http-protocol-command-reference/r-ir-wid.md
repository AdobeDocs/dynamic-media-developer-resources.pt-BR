---
description: Largura da imagem de resposta. Especifica o dimensionamento da imagem renderizada para que a imagem de resposta não seja maior do que o valor especificado, mantendo a proporção da imagem.
seo-description: Largura da imagem de resposta. Especifica o dimensionamento da imagem renderizada para que a imagem de resposta não seja maior do que o valor especificado, mantendo a proporção da imagem.
seo-title: wid
solution: Experience Manager
title: wid
uuid: 9a58a5d2-43ac-44db-9959-ba166006b7df
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---


# wid{#wid}

Largura da imagem de resposta. Especifica o dimensionamento da imagem renderizada para que a imagem de resposta não seja maior do que o valor especificado, mantendo a proporção da imagem.

`wid= *`val`*`

<table id="simpletable_1C898A7B99114BE986EC5553F6A31E82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Largura da imagem em pixels (int maior que 0). </p></td> 
 </tr> 
</table>

A imagem não é preenchida se `wid=` e `hei=` forem especificadas e `wid`/ `hei` forem diferentes da proporção da imagem.

`wid=` e  `hei=` trabalhar em conjunto para definir o tamanho da imagem retornada pelo servidor. Se `scl=` vier depois de `wid=` ou `hei=` no URL, ele cancelará esses comandos e `scl=` definirá o tamanho da imagem retornada pelo servidor.

No entanto, se `wid=` ou `hei=` vier após `scl=` no URL, eles cancelarão `scl=` e `wid=`/ `hei=` definirão o tamanho da imagem retornada pelo servidor.

>[!NOTE]
>
>Um erro será retornado se o tamanho da imagem de resposta calculada ou padrão for maior que `attribute::MaxPix`.

## Propriedades {#section-2d067c6d371748e19cb157684700a49d}

Pode ocorrer em qualquer lugar dentro da solicitação. Redimensionar a imagem com `wid=`, `hei=` ou `scl=` não altera o valor de resolução de impressão incorporado na imagem de resposta. Ignorado se `scl=` ocorrer após `wid=` ou `hei=` na sequência de comandos.

## Padrão {#section-c7c6efa03d864592a3398b6f1de5a0b0}

Se `wid=`, `hei=` ou `scl=` não forem especificadas, a imagem de resposta será dimensionada para se ajustar ao tamanho definido por `attribute::DefaultPix`. Se `attribute::DefaultPix` estiver vazio, a imagem de resposta terá o mesmo tamanho que a imagem de exibição da vinheta.

## Consulte também {#section-450dfc12b1d440e2a3172a69d91db51f}

[atributo: DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ,  [atributo::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29),  [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
