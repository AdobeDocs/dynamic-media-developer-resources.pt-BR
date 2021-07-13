---
description: O IS fornece mecanismos para simplificar o uso de mapas de imagem HTML. Os visualizadores baseados em JAVA e em Flashes no IS também incluem suporte limitado para mapas de imagem.
solution: Experience Manager
title: Mapas de imagens
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Mapas de imagens{#image-maps}

O IS fornece mecanismos para simplificar o uso de mapas de imagem HTML. Os visualizadores baseados em JAVA e em Flashes no IS também incluem suporte limitado para mapas de imagem.

Os mapas de imagem de origem são fornecidos ao IS via `catalog::Map` ou com o comando `map=`, e os mapas processados são recuperados usando o comando `req=map`.

Um mapa de imagem consiste em um ou mais elementos HTML AREA, delimitados adequadamente com &#39;&lt;&#39; e &#39;>&#39;. Se fornecido por catálogo::Mapa, todos os valores das coordenadas de pixel estão na resolução da imagem original e em relação ao canto superior esquerdo da imagem de origem (não modificada). Quando fornecido por meio de um comando `map=`, os valores de coordenada são considerados coordenadas de camada, em relação ao canto superior esquerdo da camada (após `rotate=` e `extend=`).

>[!NOTE]
>
>As coordenadas % não são permitidas no momento e podem ser processadas incorretamente.

O IS gera um mapa de imagem composta a partir dos mapas de imagem de origem de cada camada constituinte, aplicando as transformações espaciais (como escala e rotação) às coordenadas do mapa e montando os mapas de camada processados na ordem z apropriada (frente para trás) e com o posicionamento apropriado.

Os seguintes comandos são considerados para o processamento do mapa de imagem quando fornecidos em conjunto com `req=map` (diretamente na solicitação, por meio de templates de catálogo ou em `catalog::Modifier` strings):

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

Os atributos `SHAPE` e `COORDS` de um `AREA` podem ser modificados durante o processamento de uma solicitação `req=map`, todos os outros atributos do elemento `AREA` são transmitidos sem modificação. Na maioria dos casos, isso envolve alterar o valor `SHAPE` de `DEFAULT` para `RECT` (isso também adicionaria o atributo `COORDS`) ou alterar os valores `COORDS`.

Todos os elementos `AREA` que ficarem vazios durante o processamento serão removidos por completo. Se um mapa estiver associado a `layer=comp`, ele será colocado atrás de todos os outros mapas. Os dados são retornados no formulário de texto um como ou mais elementos HTML `AREA` . Uma string de resposta vazia indica que não existe nenhum mapa de imagem para os objetos especificados.

A transparência da camada não é considerada para processamento de mapa. Uma camada totalmente transparente ainda pode ter um mapa de imagem associado a ela. O mapa de uma camada parcialmente transparente não será recortado para as regiões transparentes.

## Consulte também {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) ,  [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), Especificação  [HTML 4.01](http://www.w3.org/TR/html401/)
