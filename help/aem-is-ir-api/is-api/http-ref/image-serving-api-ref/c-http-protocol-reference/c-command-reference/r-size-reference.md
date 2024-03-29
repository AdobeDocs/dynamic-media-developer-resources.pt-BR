---
title: tamanho
description: Tamanho da camada. Especifica o tamanho ou o tamanho máximo da camada para uma camada, antes de girar=, perspectiva= e estender= serem aplicados à camada.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55feeb32-b69d-4b95-80fb-c77f2612d255
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# tamanho{#size}

Tamanho da camada. Especifica o tamanho ou o tamanho máximo da camada para uma camada, antes de girar=, perspectiva= e estender= serem aplicados à camada.

` size= *`largura`*, *`altura`*`

` sizeN= *`widthN`*, *`heightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> largura </span>, <span class="varname"> altura </span> </span> </p> </td> 
  <td class="stentry"> <p>Restrição de tamanho de camada em pixels (int, int, 0 ou maior). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> widthN </span>, <span class="varname"> heightN </span> </span> </p> </td> 
  <td class="stentry"> <p>A restrição de tamanho da camada é normalizada em relação ao tamanho da camada 0 (real, real, 0,0...1,0). </p> </td> 
 </tr> 
</table>

Quando especificado para uma camada de imagem, size= restringe a largura, a altura ou ambos da imagem da camada. A imagem é dimensionada para não ser maior que `size=`. Se um tamanho normalizado for especificado, ele será relativo ao tamanho da camada 0. Se ambos *`width`* e *`height`* forem especificados, a imagem de origem será dimensionada (após `crop=` é aplicado) de forma que nenhuma dimensão exceda o tamanho especificado. A proporção do retângulo de origem é mantida em todos os casos. Ou *`width`* ou *`height`* pode ser definido como 0; nesse caso, o valor é calculado pelo servidor com base na proporção da imagem.

Quando especificado para uma camada de texto, `size=` especifica o tamanho da caixa de texto. *`width`* é obrigatório; *`height`* pode ser definido como 0, nesse caso, a altura do texto disposto será usada como a altura da camada. Por padrão, os mecanismos de layout de texto inserem quebras de linha para garantir que o texto sempre se ajuste horizontalmente no espaço disponível. Se *`height`* for especificada, as linhas que não se encaixarem no espaço disponível serão cortadas ( `text=`) ou omitido ( `textPs=`). `text=` suporta modos de ajuste adicionais; consulte `textAttr=` para obter detalhes.

Quando especificado para uma camada de cor sólida, `size=` define o tamanho exato da camada; ambos os valores devem ser especificados (a menos que uma máscara seja fornecida). Se `mask=` também é especificada, a imagem da máscara é dimensionada para caber `size=` da mesma forma que as imagens são dimensionadas em camadas de imagem.

## Propriedades {#section-5f254b66fcba49bcb63f9c9ea40b230c}

Atributo de camada. Aplica-se à camada 0 se `layer=comp`. `sizeN=` não é permitido para `layer=0` ou `layer=comp`. `sizeN=` é permitido para `layer=0` e `layer=comp` apenas em registros de catálogo que definem imagens de marca d&#39;água. Nesse caso, `sizeN` define o dimensionamento da imagem de marca d&#39;água em relação à imagem composta à qual a marca d&#39;água está sendo aplicada. Se `size=` é especificado, `res=` e `scale=` são ignoradas para esta camada. Ignorado pelas camadas de efeito.

## Padrão {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`, o tamanho da camada não é restrito. Para camadas de imagem, o tamanho da camada é determinado com base no tamanho da imagem da camada após qualquer `crop=`, `scale=`ou `res=` operações foram aplicadas. Para camadas de texto, se `size=` não for especificada, a camada será dimensionada automaticamente para se ajustar ao texto renderizado.

Camadas de cores sólidas exigem um formato totalmente especificado `size=`, um `mask=`ou `clipPath=`.

## Exemplo {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

Consulte [Exemplo A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consulte também {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) , [res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [Camadas de texto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
