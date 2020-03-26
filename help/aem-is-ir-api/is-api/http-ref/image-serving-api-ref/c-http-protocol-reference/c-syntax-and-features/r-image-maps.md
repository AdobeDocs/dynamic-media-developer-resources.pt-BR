---
description: O IS fornece mecanismos para simplificar o uso de mapas de imagem HTML. Os visualizadores baseados em JAVA e Flash no IS também incluem suporte limitado para mapas de imagem.
seo-description: O IS fornece mecanismos para simplificar o uso de mapas de imagem HTML. Os visualizadores baseados em JAVA e Flash no IS também incluem suporte limitado para mapas de imagem.
seo-title: Mapas de imagem
solution: Experience Manager
title: Mapas de imagem
topic: Scene7 Image Serving - Image Rendering API
uuid: 2b7b620b-712b-4110-ba38-993a354c09d3
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# Mapas de imagem{#image-maps}

O IS fornece mecanismos para simplificar o uso de mapas de imagem HTML. Os visualizadores baseados em JAVA e Flash no IS também incluem suporte limitado para mapas de imagem.

Os mapas de imagem de origem são fornecidos ao IS via `catalog::Map` ou com o `map=` comando, e os mapas processados são recuperados usando o `req=map` comando.

Um mapa de imagem consiste em um ou mais elementos de ÁREA HTML, devidamente delimitados com &#39;&lt;&#39; e &#39;>&#39;. Se fornecido por catálogo::Mapa, todos os valores de coordenadas de pixel são considerados na resolução original da imagem e relativos ao canto superior esquerdo da imagem de origem (não modificada). Quando fornecido por meio de um `map=` comando, os valores de coordenada são considerados coordenadas de camada, em relação ao canto superior esquerdo da camada (depois `rotate=` e `extend=`).

>[!NOTE] {class=&quot;- tópico/observação &quot;}
>
>No momento, as coordenadas % não são permitidas e podem ser processadas incorretamente.

O IS gera um mapa de imagem composto a partir dos mapas de imagem de origem de cada camada constituinte, aplicando as transformações espaciais (como escala e rotação) às coordenadas do mapa e, em seguida, montando os mapas de camada processados na ordem z apropriada (da frente para trás) e com o posicionamento apropriado.

Os comandos a seguir são considerados para o processamento do mapa de imagem quando fornecidos em conjunto com `req=map` (seja diretamente na solicitação, por meio de modelos de catálogo ou em `catalog::Modifier` strings):

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

Os atributos `SHAPE` e `COORDS` de um `AREA` podem ser modificados durante o processamento de um `req=map` pedido, todos os outros atributos do `AREA` elemento são transmitidos sem modificação. Na maioria dos casos, isso envolve alterar o `SHAPE` valor de `DEFAULT` para `RECT` (isso também adicionaria o `COORDS` atributo) ou alterar os `COORDS` valores.

Todos os `AREA` elementos que ficam vazios durante o processamento serão removidos totalmente. Se um mapa estiver associado a ele, `layer=comp` ele será colocado atrás de todos os outros mapas. Os dados são retornados no formato de texto um como ou mais elementos HTML. `AREA` Uma string de resposta vazia indica que não existe mapa de imagem para os objetos especificados.

A transparência de camada não é considerada para processamento de mapa. Uma camada totalmente transparente ainda pode ter um mapa de imagem associado a ela. O mapa de uma camada parcialmente transparente não será cortado para as regiões transparentes.

## Consulte também {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [catálogo::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), especificação [HTML 4.01](http://www.w3.org/TR/html401/)
