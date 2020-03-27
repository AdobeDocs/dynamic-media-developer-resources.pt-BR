---
description: Girar imagem. Gira a imagem, o texto ou a camada de cor sólida de acordo com o ângulo especificado.
seo-description: Girar imagem. Gira a imagem, o texto ou a camada de cor sólida de acordo com o ângulo especificado.
seo-title: girar
solution: Experience Manager
title: girar
topic: Scene7 Image Serving - Image Rendering API
uuid: 160d3c4b-3871-43bd-a17d-96198c7ea839
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# girar{#rotate}

Girar imagem. Gira a imagem, o texto ou a camada de cor sólida de acordo com o ângulo especificado.

`rotate= *`ângulo`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ângulo</span> </p> </td> 
  <td class="stentry"> <p>Ângulo de rotação em graus (real). </p></td> 
 </tr> 
</table>

Ângulos positivos giram no sentido horário. O ponto de ancoragem da camada ( `anchor=` ou `catalog::Anchor`) serve como o centro de rotação. O retângulo da camada é ampliado e ajustado ao redor dos dados girados conforme necessário para evitar recortes. A rotação é aplicada após o preenchimento da área de plano de fundo da camada com `color=`. `bgColor=` pode ser usado para adicionar cor de plano de fundo ao retângulo delimitador após a rotação.

## Propriedades {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

comando Camada. Aplica-se à camada atual ou à camada 0, se `layer=comp`. Ignorado pelas camadas de efeito.

## Padrão {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`, sem rotação.

## Example {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

Coloque um rótulo &quot;À venda&quot; próximo ao canto superior esquerdo das imagens em um catálogo de imagens. A imagem do rótulo já está dimensionada corretamente para a visualização 300x300 e deve ser girada 30 graus para a esquerda. Preencha a caixa de texto com uma cor branca e semiopaca para aprimorar o rótulo.

`http:// *`server`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

Aplica-se `size=` à camada 0 para definir o tamanho da visualização, em vez de usar `wid=` e `hei=`. Isso permite `myImageId` o redimensionamento sem alterar o tamanho final de `labelImage`. Também é necessário especificar `scl=1`, caso contrário, a imagem composta poderá ser dimensionada para `attribute::DefaultPix` (a menos que seja definida como 0,0). `color=` adiciona a cor de plano de fundo semiopaca à caixa de texto antes da rotação.

A origem para ambas as camadas é definida nos cantos superior esquerdo, para alcançar o alinhamento desejado. Observe que o ponto de origem da camada 1 se aplica a `labelImage`depois de girado.

Consulte [Exemplo A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) em [Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) para obter um exemplo de texto girado.

## Consulte também {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
