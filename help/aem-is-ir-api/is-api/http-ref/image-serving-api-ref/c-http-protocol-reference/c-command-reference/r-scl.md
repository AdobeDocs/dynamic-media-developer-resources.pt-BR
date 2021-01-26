---
description: Dimensionar visualização. Dimensiona a imagem composta pelo inverso de renceFactor.
seo-description: Dimensionar visualização. Dimensiona a imagem composta pelo inverso de renceFactor.
seo-title: scl
solution: Experience Manager
title: scl
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 10a365dc-9fc1-4236-9528-4aca04a4ca19
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---


# scl{#scl}

Dimensionar visualização. Dimensiona a imagem composta pelo inverso de renceFactor.

`scl= *`renceFactor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> renceFactor</span> </p> </td> 
  <td class="stentry"> <p>Fator de escala inverso (real maior que 0,0). </p></td> 
 </tr> 
</table>

Nenhum dimensionamento é aplicado quando `scl=1`. *`invFactor`* maior que 1,0 de escala reduzida e menor que 1,0 amplia a imagem composta.

Se `scl=` for especificado e `wid=` e/ou `hei=` também estiverem presentes, a imagem será cortada para `wid=` e/ou `hei=` após o dimensionamento.

>[!NOTE]
>
>Um erro será retornado se o tamanho da imagem de resposta calculada ou padrão for maior que `attribute::MaxPix`.

## Propriedades {#section-60af012719db477db4a4703e9a6da5f5}

Atributo de visualização. Aplica-se independentemente da configuração de camada atual.

## Padrão {#section-32502fa218a24e1f9c65f41c0260b56a}

Se `wid=`, `hei=` ou `scl=` não forem especificados, a imagem de resposta terá o tamanho da imagem composta ou `attribute::DefaultPix`, o que for menor.

## Exemplo {#section-a33f6239476a4b438d939656ad99aa76}

Consulte o exemplo em [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) para obter um aplicativo comum de `scl=`.

## Consulte também {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [atributo::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
