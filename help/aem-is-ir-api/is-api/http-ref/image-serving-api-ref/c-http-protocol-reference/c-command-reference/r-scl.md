---
title: scl
description: Modo de exibição de escala. Dimensiona a imagem composta pelo inverso de invFactor.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 297d187c-3a52-45ff-b73d-0b0e4b956080
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# scl{#scl}

Modo de exibição de escala. Dimensiona a imagem composta pelo inverso de invFactor.

`scl= *`invFactor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> invFactor</span> </p> </td> 
  <td class="stentry"> <p>Fator de escala inversa (real maior que 0,0). </p></td> 
 </tr> 
</table>

Nenhum dimensionamento é aplicado quando `scl=1`. Um valor de *`invFactor`* maior que 1,0 para baixo-escala e menor que 1,0 aumenta a imagem composta.

Se `scl=` for especificado, e `wid=` e/ou `hei=` também estiverem presentes, a imagem será cortada para `wid=` e/ou `hei=` após o dimensionamento.

>[!NOTE]
>
>Um erro será retornado se o tamanho da imagem de resposta calculada ou padrão for maior que `attribute::MaxPix`.

## Propriedades {#section-60af012719db477db4a4703e9a6da5f5}

Exibir atributo. Ela se aplica independentemente da configuração atual da camada.

## Padrão {#section-32502fa218a24e1f9c65f41c0260b56a}

Se `wid=`, `hei=` ou `scl=` não forem especificados, a imagem de resposta terá o tamanho da imagem composta ou `attribute::DefaultPix`, o que for menor.

## Exemplo {#section-a33f6239476a4b438d939656ad99aa76}

Veja o exemplo em [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) para um aplicativo comum de `scl=`.

## Consulte também {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
