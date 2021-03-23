---
description: Visualização de escala. Dimensiona a imagem composta pelo inverso de renceFactor.
seo-description: Visualização de escala. Dimensiona a imagem composta pelo inverso de renceFactor.
seo-title: scl
solution: Experience Manager
title: scl
uuid: 10a365dc-9fc1-4236-9528-4aca04a4ca19
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---


# scl{#scl}

Visualização de escala. Dimensiona a imagem composta pelo inverso de renceFactor.

`scl= *`renceFactor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> renceFactor</span> </p> </td> 
  <td class="stentry"> <p>Fator de escala inverso (real superior a 0,0). </p></td> 
 </tr> 
</table>

Nenhum dimensionamento é aplicado quando `scl=1`. *`invFactor`* maior que 1,0 de escala baixa e menor que 1,0 amplia a imagem composta.

Se `scl=` for especificado, e `wid=` e/ou `hei=` também estiverem presentes, a imagem será cortada para `wid=` e/ou `hei=` após o dimensionamento.

>[!NOTE]
>
>Um erro será retornado se o tamanho da imagem de resposta calculada ou padrão for maior que `attribute::MaxPix`.

## Propriedades {#section-60af012719db477db4a4703e9a6da5f5}

Exibir atributo. Aplica-se independentemente da configuração de camada atual.

## Padrão {#section-32502fa218a24e1f9c65f41c0260b56a}

Se `wid=`, `hei=` ou `scl=` não forem especificadas, a imagem de resposta terá o tamanho da imagem composta ou `attribute::DefaultPix`, o que for menor.

## Exemplo {#section-a33f6239476a4b438d939656ad99aa76}

Veja o exemplo em [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) para uma aplicação comum de `scl=`.

## Consulte também {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [atributo::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
