---
title: scl
description: Visualização de escala. Dimensiona a imagem renderizada pelo fator de escala especificado, em relação à vinheta de resolução completa.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e36db25c-af45-4256-b982-b7b06b87f5f9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# scl{#scl}

Visualização de escala. Dimensiona a imagem renderizada pelo fator de escala especificado, em relação à vinheta de resolução completa.

`scl= *`renceFactor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renceFactor</span> </span> </p></td> 
  <td class="stentry"> <p>Fator de escala inverso (real, 1,0 ou superior). </p></td> 
 </tr> 
</table>

If `scl=` come `wid=` ou `hei=` no URL, ele cancela esses comandos e `scl=` define o tamanho da imagem retornada pelo servidor.

No entanto, se `wid=` ou `hei=` come `scl=` no URL, eles cancelam `scl=` e `wid=`/ `hei=` defina o tamanho da imagem retornada pelo servidor.

>[!NOTE]
>
>Um erro é retornado se o tamanho da imagem de resposta calculada ou padrão for maior que `attribute::MaxPix`.

## Propriedades {#section-170458cbd6984bd59a3434431258b20f}

Pode ocorrer em qualquer lugar dentro da solicitação. Ignorado se `wid=` ou `hei=` ocorrer após `scl=` na sequência de comandos.

Redimensionar a imagem com `scl=` não altera o valor de resolução de impressão incorporado na imagem de resposta.

## Padrão {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

If `wid=`, `hei=`ou `scl=` não forem especificadas, a imagem de resposta será dimensionada para se ajustar ao tamanho definido por `attribute::DefaultPix`. If `attribute::DefaultPix` estiver vazia, a imagem de resposta terá o mesmo tamanho que a imagem de exibição da vinheta.

## Consulte também {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3), [atributo::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [atributo::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
