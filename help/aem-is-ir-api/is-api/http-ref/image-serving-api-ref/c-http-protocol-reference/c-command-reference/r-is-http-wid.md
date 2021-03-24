---
description: Largura da exibição. Especifica a largura da imagem de resposta (imagem de exibição) quando fit= não está presente na solicitação.
solution: Experience Manager
title: wid
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---


# wid{#wid}

Largura da exibição. Especifica a largura da imagem de resposta (imagem de exibição) quando fit= não está presente na solicitação.

` wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>Largura da imagem em pixels (int maior que 0). </p> </td> 
 </tr> 
</table>

Se `hei=` e `scl=` forem especificadas, a imagem composta poderá ser cortada de acordo com o atributo `align=`. Quando `fit=` está presente, `wid=` especifica a largura exata, mínima ou máxima da imagem de resposta; consulte a descrição de `fit=` para obter detalhes.

Se `scl=` não for especificado, a imagem composta será dimensionada para se ajustar. Se `wid=` e `hei=` forem especificadas e `scl=` não forem especificadas, a imagem será dimensionada para caber inteiramente no retângulo largura/altura, deixando a menor área de fundo possível exposta. Nesse caso, a imagem é posicionada no retângulo de exibição de acordo com o atributo `align=`.

>[!NOTE]
>
>Um erro será retornado se o tamanho da imagem de resposta calculada ou padrão for maior que `attribute::MaxPix`.

## Padrão {#section-976d4c8554a34c899f85d172f6ac6f58}

Se `wid=`, `hei=` ou `scl=` não forem especificadas, a imagem de resposta terá o tamanho da imagem composta ou `attribute::DefaultPix`, o que for menor.

## Propriedades {#section-c93b7ce1b0d2475f80b06264b45d1285}

Exibir atributo. Aplica-se independentemente da configuração de camada atual.

## Exemplo {#section-82bc98b7c15a451bbe9b915d414c0470}

Solicite uma imagem para ajustá-la a um retângulo de 200x200; no canto superior direito alinhe a imagem se ela não for quadrada. Qualquer área de plano de fundo é preenchida com `attribute::BkgColor`.

` http:// *`server`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

A mesma imagem, entregue em uma largura fixa de 200 pixels, mas com uma altura variável para manter a proporção da imagem. Nesse caso, a imagem retornada nunca tem nenhuma área de preenchimento do plano de fundo. Observe que, nesse caso, align= não teria efeito algum.

` http:// *`server`*/myRootId/myImageId?wid=200`

## Consulte também {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) ,  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7),  [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1),  [atributo::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
