---
title: scl
description: Modo de exibição de escala. Dimensiona a imagem renderizada pelo fator de escala especificado, em relação à vinheta de resolução total.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e36db25c-af45-4256-b982-b7b06b87f5f9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---

# scl{#scl}

Modo de exibição de escala. Dimensiona a imagem renderizada pelo fator de escala especificado, em relação à vinheta de resolução total.

`scl= *`invFactor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> invFactor</span> </span> </p></td> 
  <td class="stentry"> <p>Fator de escala inversa (real, 1,0 ou maior). </p></td> 
 </tr> 
</table>

Se `scl=` vier depois de `wid=` ou `hei=` na URL, ele cancelará esses comandos e `scl=` definirá o tamanho da imagem retornada pelo servidor.

No entanto, se `wid=` ou `hei=` vir depois de `scl=` na URL, eles cancelam `scl=` e `wid=`/ `hei=` definem o tamanho da imagem retornada pelo servidor.

>[!NOTE]
>
>Um erro será retornado se o tamanho da imagem de resposta calculada ou padrão for maior que `attribute::MaxPix`.

## Propriedades {#section-170458cbd6984bd59a3434431258b20f}

Pode ocorrer em qualquer lugar na solicitação. Ignorado se `wid=` ou `hei=` ocorrer após `scl=` na sequência de comandos.

O redimensionamento da imagem com `scl=` não altera o valor da resolução de impressão inserido na imagem de resposta.

## Padrão {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

Se `wid=`, `hei=` ou `scl=` não forem especificados, a imagem de resposta será dimensionada para se ajustar ao tamanho definido por `attribute::DefaultPix`. Se `attribute::DefaultPix` estiver vazio, a imagem de resposta terá o mesmo tamanho que a imagem de exibição da vinheta.

## Consulte também {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3), [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
