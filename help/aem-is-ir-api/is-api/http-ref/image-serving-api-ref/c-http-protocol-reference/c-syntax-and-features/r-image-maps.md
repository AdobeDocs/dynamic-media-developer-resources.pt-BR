---
description: O IS fornece mecanismos para simplificar o uso de mapas de imagem do HTML. Os visualizadores baseados em JAVA e em Flash no IS também incluem suporte limitado para mapas de imagem.
solution: Experience Manager
title: Mapas de imagem
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Mapas de imagem{#image-maps}

O IS fornece mecanismos para simplificar o uso de mapas de imagem do HTML. Os visualizadores baseados em JAVA e em Flash no IS também incluem suporte limitado para mapas de imagem.

Os mapas de imagem de Source são fornecidos ao IS por meio de `catalog::Map` ou com o comando `map=`, e os mapas processados são recuperados usando o comando `req=map`.

Um mapa de imagem consiste em um ou mais elementos HTML AREA, delimitados corretamente com &#39;&lt;&#39; e &#39;>&#39;. Se fornecido por meio de catalog::Map, todos os valores de coordenadas de pixel são considerados como estando na resolução da imagem original e relativos ao canto superior esquerdo da imagem de origem (não modificada). Quando fornecido por meio de um comando `map=`, presume-se que os valores de coordenadas sejam coordenadas de camada, relativas ao canto superior esquerdo da camada (após `rotate=` e `extend=`).

>[!NOTE]
>
>% de coordenadas não são permitidas neste momento e podem ser processadas incorretamente.

IS gera um mapa de imagem composta a partir dos mapas de imagem de origem de cada camada constituinte aplicando as transformações espaciais (como dimensionamento e rotação) às coordenadas do mapa e, em seguida, montando os mapas de camada processados na ordem z apropriada (da frente para trás) e com o posicionamento apropriado.

Os seguintes comandos são considerados para processamento de mapa de imagem quando fornecidos em conjunto com `req=map` (diretamente na solicitação, por meio de modelos de catálogo ou em `catalog::Modifier` cadeias de caracteres):

* `align=`
* `wid=`
* `hei=`
* `scl=`
* `crop=`
* `flip=`
* `rotate=`
* `scale=`
* `layer=`
* `size=`
* `extend=`
* `origin=`
* `pos=`
* `anchor=`
* `src=`
* `map=`

Todos os outros comandos são efetivamente ignorados.

Os atributos `SHAPE` e `COORDS` de um `AREA` podem ser modificados durante o processamento de uma solicitação `req=map`. Todos os outros atributos do elemento `AREA` são passados sem modificação. Na maioria dos casos isso envolve alterar o valor `SHAPE` de `DEFAULT` para `RECT` (isso também adicionaria o atributo `COORDS`) ou alterar os valores `COORDS`.

Quaisquer elementos `AREA` que ficarem vazios durante o processamento serão totalmente removidos. Se um mapa estiver associado a `layer=comp`, ele será colocado atrás de todos os outros mapas. Os dados são retornados em forma de texto como um ou mais elementos do HTML `AREA`. Uma cadeia de caracteres de resposta vazia indica que não existe mapa de imagem para os objetos especificados.

A transparência de camada não é considerada para o processamento do mapa. Uma camada totalmente transparente ainda pode ter um mapa de imagem associado a ela. O mapa de uma camada parcialmente transparente não é recortado para as regiões transparentes.

## Consulte também {#see-also}

[mapa=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [catálogo::Mapa](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [Especificação do HTML 4.01](https://www.w3.org/TR/html401/)
