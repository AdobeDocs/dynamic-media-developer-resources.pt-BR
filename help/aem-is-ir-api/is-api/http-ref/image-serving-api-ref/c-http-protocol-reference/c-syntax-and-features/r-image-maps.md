---
description: IS fornece mecanismos para simplificar o uso de mapas de imagem HTML. Os visualizadores baseados em JAVA e em Flashes no IS também incluem suporte limitado para mapas de imagem.
solution: Experience Manager
title: Mapas de imagens
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# Mapas de imagens{#image-maps}

IS fornece mecanismos para simplificar o uso de mapas de imagem HTML. Os visualizadores baseados em JAVA e em Flashes no IS também incluem suporte limitado para mapas de imagem.

Os mapas de imagem de origem são fornecidos ao IS por meio de `catalog::Map` ou com a `map=` e os mapas processados são recuperados usando o `req=map` comando.

Um mapa de imagem consiste em um ou mais elementos HTML AREA, delimitados adequadamente com &#39;&lt;&#39; e &#39;>&#39;. Se fornecido por catálogo::Mapa, todos os valores das coordenadas de pixel estão na resolução da imagem original e em relação ao canto superior esquerdo da imagem de origem (não modificada). Quando fornecido através de um `map=` , os valores de coordenadas são considerados coordenadas de camada em relação ao canto superior esquerdo da camada (após `rotate=` e `extend=`).

>[!NOTE]
>
>As coordenadas % não são permitidas no momento e podem ser processadas incorretamente.

O IS gera um mapa de imagem composta a partir dos mapas de imagem de origem de cada camada constituinte, aplicando as transformações espaciais (como escala e rotação) às coordenadas do mapa e montando os mapas de camada processados na ordem z apropriada (frente para trás) e com o posicionamento apropriado.

Os seguintes comandos são considerados para o processamento do mapa de imagem quando fornecido junto com o `req=map` (diretamente na solicitação, por meio de templates de catálogo ou em `catalog::Modifier` strings):

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

O `SHAPE` e `COORDS` atributos de um `AREA` podem ser alteradas durante a transformação de um `req=map` solicitação, todos os outros atributos do `AREA` são transmitidos sem modificação. Na maioria dos casos, isso envolve alterar o `SHAPE` valor de `DEFAULT` para `RECT` (isso também adicionaria a variável `COORDS` ) ou alterar o `COORDS` valores.

Qualquer `AREA` os elementos que ficam vazios durante o processamento são removidos totalmente. Se um mapa estiver associado a `layer=comp` é colocado atrás de todos os outros mapas. Os dados são retornados no formulário de texto um como ou mais HTML `AREA` elementos. Uma string de resposta vazia indica que não existe nenhum mapa de imagem para os objetos especificados.

A transparência da camada não é considerada para processamento de mapa. Uma camada totalmente transparente ainda pode ter um mapa de imagem associado a ela. O mapa de uma camada parcialmente transparente não será recortado para as regiões transparentes.

## Consulte também {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [catálogo::Mapa](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [HTML 4.01 Especificação](https://www.w3.org/TR/html401/)
