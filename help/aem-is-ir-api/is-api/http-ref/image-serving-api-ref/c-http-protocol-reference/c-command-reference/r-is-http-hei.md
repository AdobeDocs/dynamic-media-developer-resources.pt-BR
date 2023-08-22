---
title: hei
description: Altura da exibição. Especifica a altura da imagem de resposta (imagem de exibição) quando o ajuste não está presente na solicitação.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c812c7f0-4ac1-42cb-be47-7baebd8caf60
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---

# hei{#hei}

Altura da exibição. Especifica a altura da imagem de resposta (imagem de exibição) quando o ajuste não está presente na solicitação.

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>Altura da imagem em pixels (int maior que 0). </p> </td> 
 </tr> 
</table>

Se ambos `wid=` e `scl=` forem especificadas, a imagem composta poderá ser cortada de acordo com as `align=`atributo. Quando `fit=` está presente, `hei=` especifica a altura exata, mínima ou máxima da imagem de resposta; consulte a descrição de [fit=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md) para obter detalhes.

Se `scl=` não for especificada, a imagem composta será dimensionada para caber. Se ambos `wid=` e `hei=` são especificados e `scl=` não for especificada, a imagem é dimensionada para caber inteiramente no retângulo wid/hei, deixando a menor área de fundo exposta possível; nesse caso, a imagem é posicionada dentro do retângulo de visualização de acordo com a `align=` atributo. A área de plano de fundo é preenchida com `bgc=`, ou, se não especificado com `attribute::BkgColor`.

>[!NOTE]
>
>Um erro será retornado se o tamanho da imagem de resposta calculada for maior que `attribute::MaxPix`.

## Propriedades {#section-534923644a1e464496eeba83dedcbd3c}

Exibir atributo. Aplica-se independentemente da configuração da camada atual.

## Padrão {#section-76544d34806d4124a8b173e229cba71f}

Se nenhuma delas `wid=`, `hei=`, nem `scl=` forem especificados, a imagem de resposta terá o tamanho da imagem composta ou `attribute::DefaultPix`, o que for menor.

## Exemplos {#section-eb10df7cd67e4733984810aaffd0b9e2}

Solicite uma imagem para ajustá-la a um retângulo de 200x200; alinhe a imagem na parte superior esquerda se ela não for quadrada. Qualquer área do plano de fundo é preenchida com `attribute::BkgColor`.

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

A mesma imagem, entregue em uma altura fixa de 200 pixels, mas com uma largura variável para corresponder à proporção da imagem. Nesse caso, a imagem retornada nunca tem áreas de preenchimento do plano de fundo. Observe que, nesse caso `align=` não teria qualquer efeito.

`http://server/myRootId/myImageId?hei=200`

## Consulte também {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
