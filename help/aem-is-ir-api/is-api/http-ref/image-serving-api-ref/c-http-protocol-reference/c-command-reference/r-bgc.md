---
description: Cor do fundo da visualização. Especifica a cor de plano de fundo para a imagem composta (imagem de visualização).
seo-description: Cor do fundo da visualização. Especifica a cor de plano de fundo para a imagem composta (imagem de visualização).
seo-title: bgc
solution: Experience Manager
title: bgc
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 3ea8291e-3223-45ff-a2ad-43fc212eff90
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---


# bgc{#bgc}

Cor do fundo da visualização. Especifica a cor de plano de fundo para a imagem composta (imagem de visualização).

`bgc= *`cor`*`

<table id="simpletable_998CF426296945FEA48D19E33B71A17E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cor</span></span> </p> </td> 
  <td class="stentry"> <p>Valor de cor cinza, RGB ou CMYK. </p></td> 
 </tr> 
</table>

Especifica uma cor de preenchimento opaca a ser usada para o plano de fundo da visualização. Visível somente se a imagem composta tiver áreas transparentes ou se a imagem composta tiver uma proporção diferente do retângulo da visualização. Ignorado se `fmt=tif-alpha` ou `fmt=png-alpha`, ou `req=mask`.

>[!NOTE]
>
>O sufixo de cor &#39;s&#39; é ignorado por `bgc=`. Os valores de cor especificados com `bgc=` estão sempre associados ao respectivo espaço de cor de saída.

## Propriedades {#section-b729b50b1ea7433b82ba34ecd61839cd}

Atributo de visualização. Aplica-se independentemente da configuração de camada atual. Ignorado se `req=mask`, `fmt=tif-alpha`, `fmt=png-alpha`, `fmt=gif-alpha` ou `fmt=swf-alpha`.

Qualquer valor alfa especificado com cor é ignorado.

*`color`* é considerado como pertencendo ao espaço de cor de saída (conforme especificado com  `icc=`) e deve ter o mesmo tipo de pixel da imagem de saída. Se os tipos de pixels não corresponderem, *`color`* será convertido usando conversão ingênua.

## Padrão {#section-4e025cbd723547b5ab4450f7aad70da3}

`attribute::BkgColor`.

## Exemplo {#section-7bcdfbc0e1274e86a69d39186b090789}

Especifique uma cor de plano de fundo explícita para uma solicitação de miniatura:

`http://server/myRootId/myImageId?req=tmb&bgc=214,245,130`

## Consulte também {#section-1e55f9f98f1847918a1725836a27cfaa}

[cor](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93),  [atributo::BkgColor](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-bkgcolor.md#reference-ed53106ee50442d7a2dd3e1f60e6f0f8),  [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a),  [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76),  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), Gerenciamento  [de cores](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
