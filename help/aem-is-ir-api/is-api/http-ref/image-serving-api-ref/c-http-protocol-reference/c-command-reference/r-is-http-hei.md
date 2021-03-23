---
description: Exibir Altura. Especifica a altura da imagem de resposta (imagem de exibição) quando ajuste não está presente na solicitação.
seo-description: Exibir Altura. Especifica a altura da imagem de resposta (imagem de exibição) quando ajuste não está presente na solicitação.
seo-title: hei
solution: Experience Manager
title: hei
uuid: 307952bb-604f-49b4-bce3-b7a7fc7ec63b
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---


# hei{#hei}

Exibir Altura. Especifica a altura da imagem de resposta (imagem de exibição) quando ajuste não está presente na solicitação.

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>Altura da imagem em pixels (int maior que 0). </p> </td> 
 </tr> 
</table>

Se `wid=` e `scl=` forem especificadas, a imagem composta poderá ser cortada de acordo com o atributo `align=`. Quando `fit=` está presente, `hei=` especifica a altura exata, mínima ou máxima da imagem de resposta; consulte a descrição de ` [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)` para obter detalhes.

Se `scl=` não for especificado, a imagem composta será dimensionada para se ajustar. Se `wid=` e `hei=` forem especificadas e `scl=` não forem especificadas, a imagem será dimensionada para caber inteiramente no retângulo largura/altura, deixando a menor área de fundo possível exposta; nesse caso, a imagem é posicionada no retângulo de exibição de acordo com o atributo `align=`. A área de fundo é preenchida com `bgc=` ou, se não for especificada com `attribute::BkgColor`.

>[!NOTE]
>
>Um erro será retornado se o tamanho da imagem de resposta calculada for maior que `attribute::MaxPix`.

## Propriedades {#section-534923644a1e464496eeba83dedcbd3c}

Exibir atributo. Aplica-se independentemente da configuração de camada atual.

## Padrão {#section-76544d34806d4124a8b173e229cba71f}

Se `wid=`, `hei=` ou `scl=` não forem especificadas, a imagem de resposta terá o tamanho da imagem composta ou `attribute::DefaultPix`, o que for menor.

## Exemplos {#section-eb10df7cd67e4733984810aaffd0b9e2}

Solicite uma imagem para ajustá-la a um retângulo de 200x200; alinhe a imagem no canto superior esquerdo, se ela não for quadrada. Qualquer área de plano de fundo é preenchida com `attribute::BkgColor`.

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

A mesma imagem, entregue em uma altura fixa de 200 pixels, mas com uma largura variável para corresponder à proporção da imagem. Nesse caso, a imagem retornada nunca tem nenhuma área de preenchimento do plano de fundo. Observe que, nesse caso, `align=` não teria efeito algum.

`http://server/myRootId/myImageId?hei=200`

## Consulte também {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88),  [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f),  [atributo::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1),  [atributo::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
