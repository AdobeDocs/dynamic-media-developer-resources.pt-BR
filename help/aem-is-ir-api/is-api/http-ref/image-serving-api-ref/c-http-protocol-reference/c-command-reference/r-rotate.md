---
title: girar
description: Girar imagem. Gira a imagem, o texto ou a camada de cor sólida pelo ângulo especificado.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9f1b2d6f-4e67-4530-9ec6-870b97687ce0
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# girar{#rotate}

Girar imagem. Gira a imagem, o texto ou a camada de cor sólida pelo ângulo especificado.

`rotate= *`ângulo`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ângulo</span> </p> </td> 
  <td class="stentry"> <p>Ângulo de rotação em graus (real). </p></td> 
 </tr> 
</table>

Os ângulos positivos giram no sentido horário. O ponto de ancoragem da camada ( `anchor=` ou `catalog::Anchor`) serve como centro de rotação. O retângulo da camada é aumentado e ajustado em torno dos dados girados, conforme necessário, para evitar o corte. A rotação é aplicada após preencher a área de plano de fundo da camada com `color=`. O modificador `bgColor=` pode ser usado para adicionar a cor do plano de fundo ao retângulo delimitador após a rotação.

## Propriedades {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

Camada. Se aplica à camada atual ou à camada 0 `layer=comp`. Ignorado pelas camadas de efeito.

## Padrão {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`, para nenhuma rotação.

## Exemplo {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

Coloque um rótulo &quot;Em promoção&quot; próximo ao canto superior esquerdo das imagens em um catálogo de imagens. A imagem do rótulo já está dimensionada corretamente para a exibição 300x300 e deve ser girada 30° para a esquerda. Para aprimorar o rótulo, preencha a caixa de texto com uma cor branca e semiopaca.

`http:// *`server`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

Aplicar `size=` à camada 0 para definir o tamanho da exibição, em vez de usar `wid=` e `hei=`. Este método permite `myImageId` a ser redimensionado sem alterar o tamanho final de `labelImage`. Além disso, especifique `scl=1`, caso contrário, a imagem composta poderá ser dimensionada para `attribute::DefaultPix` (a menos que seja definido como 0,0). O modificador `color=` adiciona a cor de fundo semiopaca à caixa de texto antes da rotação.

A origem de ambas as camadas é definida no canto superior esquerdo para alcançar o alinhamento desejado. O ponto de origem da camada 1 aplica-se a `labelImage`depois de girar.

Consulte [Exemplo A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) para obter um exemplo de texto girado.

## Consulte também {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
