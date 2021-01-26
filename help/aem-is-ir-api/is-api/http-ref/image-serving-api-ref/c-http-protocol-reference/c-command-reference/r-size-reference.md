---
description: Tamanho da camada. Especifica o tamanho ou o tamanho máximo da camada para uma camada, antes de rotate=, perspective= e extension= serem aplicados à camada.
seo-description: Tamanho da camada. Especifica o tamanho ou o tamanho máximo da camada para uma camada, antes de rotate=, perspective= e extension= serem aplicados à camada.
seo-title: tamanho
solution: Experience Manager
title: tamanho
topic: Dynamic Media Image Serving - Image Rendering API
uuid: c9c13062-7974-4dd9-aff4-f9502bcf442e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---


# size{#size}

Tamanho da camada. Especifica o tamanho ou o tamanho máximo da camada para uma camada, antes de rotate=, perspective= e extension= serem aplicados à camada.

` size= *``*, *`largura`*`

` sizeN= *``*, *`widthNheightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> largura  </span>,  <span class="varname"> altura  </span> </span> </p> </td> 
  <td class="stentry"> <p>Restrição do tamanho da camada em pixels (int, int, 0 ou superior). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> widthN  </span>,  <span class="varname"> heightN  </span> </span> </p> </td> 
  <td class="stentry"> <p>A restrição de tamanho da camada é normalizada em relação ao tamanho da camada 0 (real, real, 0.0...1.0). </p> </td> 
 </tr> 
</table>

Quando especificado para uma camada de imagem, size= restringe a largura, a altura ou a largura da imagem da camada, ou ambos. A imagem será dimensionada para não ser maior que `size=`. Se um tamanho normalizado for especificado, ele será relativo ao tamanho da camada 0. Se *`width`* e *`height`* forem especificados, a imagem de origem será dimensionada (após `crop=` ser aplicada) para que nenhuma dimensão exceda o tamanho especificado. A proporção do retângulo de origem é mantida em todos os casos. *`width`* ou *`height`* pode ser definido como 0; nesse caso, o valor é calculado pelo servidor com base na proporção da imagem.

Quando especificado para uma camada de texto, `size=` especifica o tamanho da caixa de texto. *`width`* é obrigatório;  *`height`* pode ser definido como 0, caso em que a altura do texto disposto é usada como a altura da camada. Por padrão, os mecanismos de layout de texto inserem quebras de linha para garantir que o texto sempre se ajuste horizontalmente no espaço disponível. Se *`height`* for especificado, as linhas que não se encaixam no espaço disponível serão cortadas ( `text=`) ou omitidas ( `textPs=`). `text=` suporta modos de ajuste adicionais; consulte  `textAttr=` para obter detalhes.

Quando especificado para uma camada de cor sólida, `size=` define o tamanho exato da camada; ambos os valores devem ser especificados (a menos que uma máscara seja fornecida). Se `mask=` também for especificado, a imagem da máscara será dimensionada para se ajustar `size=` da mesma forma que as imagens são dimensionadas em camadas de imagem.

## Propriedades {#section-5f254b66fcba49bcb63f9c9ea40b230c}

Atributo de camada. Aplica-se à camada 0 se `layer=comp`. `sizeN=` não é permitido para  `layer=0` ou  `layer=comp`. `sizeN=` é permitido para  `layer=0` e  `layer=comp` apenas em registros de catálogo que definem imagens de marca d&#39;água. Nesse caso, `sizeN` define o dimensionamento da imagem da marca d&#39;água em relação à imagem composta à qual a marca d&#39;água está sendo aplicada. Se `size=` for especificado, `res=` e `scale=` serão ignorados para esta camada. Ignorado pelas camadas de efeito.

## Padrão {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`, o tamanho da camada não está restrito. Para camadas de imagem, o tamanho da camada é determinado com base no tamanho da imagem da camada depois que qualquer operação `crop=`, `scale=` ou `res=` for aplicada. Para camadas de texto, se `size=` não for especificado, a camada será dimensionada automaticamente para se ajustar ao texto renderizado.

As camadas de cores sólidas exigem `size=`, `mask=` ou `clipPath=` totalmente especificadas.

## Exemplo {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

Consulte [Exemplo A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) em [Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consulte também {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) ,  [res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d),  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), Camadas  [de texto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
