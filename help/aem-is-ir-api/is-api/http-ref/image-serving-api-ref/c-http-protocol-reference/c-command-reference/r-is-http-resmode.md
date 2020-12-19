---
description: Modo de reamostragem. Escolhe o algoritmo de reamostragem e/ou interpolação a ser usado para dimensionar dados de imagem. Também se aplica à rotação de camadas de texto e ao redimensionamento de imagens compostas durante a transformação da visualização.
seo-description: Modo de reamostragem. Escolhe o algoritmo de reamostragem e/ou interpolação a ser usado para dimensionar dados de imagem. Também se aplica à rotação de camadas de texto e ao redimensionamento de imagens compostas durante a transformação da visualização.
seo-title: resMode
solution: Experience Manager
title: resMode
topic: Scene7 Image Serving - Image Rendering API
uuid: 8e12aa06-072c-4e7a-84e6-01437c43c57b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---


# resMode{#resmode}

Modo de reamostragem. Escolhe o algoritmo de reamostragem e/ou interpolação a ser usado para dimensionar dados de imagem. Também se aplica à rotação de camadas de texto e ao redimensionamento de imagens compostas durante a transformação da visualização.

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bilhão  </span> </p> </td> 
   <td colname="col2"> <p>Seleciona a interpolação bi-linear padrão. Método de reamostragem mais rápido; alguns artefatos de aliasing podem ser perceptíveis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bicub  </span> </p> </td> 
   <td colname="col2"> <p>Seleciona a interpolação bicúbica. Mais intensivo da CPU do que a interpolação bidirecional, mas produzirá imagens mais nítidas com artefatos de aliasing menos perceptíveis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> aguda2  </span> </p> </td> 
   <td colname="col2"> <p>Seleciona uma função Lanczos Window modificada como um algoritmo de interpolação. Pode produzir resultados ligeiramente mais nítidos do que bi-cúbicos a um custo de CPU mais alto. <span class="codeph"> O afiado  </span> foi substituído pelo  <span class="codeph"> afiado2  </span>, que tem uma probabilidade menor de causar artefatos aliasados (Moiré). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharp  </span> </p> </td> 
   <td colname="col2"> <p>Seleciona o reamostrador padrão Photoshop para reduzir o tamanho da imagem, que é chamado de "divisor bicúbico" no Adobe Photoshop. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-a171bacf4ddf43c782e46b86a16d443e}

Atributo de solicitação. Aplica-se a todas as operações de escala envolvidas na criação da imagem de resposta final, incluindo toda a escala de camadas.

## Padrão {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## Exemplo {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

Recupere uma representação de melhor qualidade de uma imagem em camadas armazenada em um catálogo de imagens. A imagem pode incluir texto. Esperamos continuar a processar em um aplicativo de edição de imagem e, portanto, solicitar um canal alfa com a imagem.

` http:// *`server`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## Consulte também {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[atributo::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
