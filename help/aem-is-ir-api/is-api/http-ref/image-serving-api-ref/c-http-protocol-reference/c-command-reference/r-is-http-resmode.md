---
description: Modo de nova amostra. Escolhe o algoritmo de reamostragem e/ou interpolação a ser usado para dimensionar dados de imagem. Também se aplica à rotação de camadas de texto e ao redimensionamento de imagens compostas durante a transformação da exibição.
solution: Experience Manager
title: resMode
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
exl-id: 63c1c028-0378-4a38-8018-e358491786d8
translation-type: tm+mt
source-git-commit: b08d1f5b0aa512be4a6e6a4d45d8d4dec15ca1db
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# resMode{#resmode}

Modo de nova amostra. Escolhe o algoritmo de reamostragem e/ou interpolação a ser usado para dimensionar dados de imagem. Também se aplica à rotação de camadas de texto e ao redimensionamento de imagens compostas durante a transformação da exibição.

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bilhão  </span> </p> </td> 
   <td colname="col2"> <p>Seleciona a interpolação bi-linear padrão. Método de reamostragem mais rápido; alguns artefatos de aliasing são perceptíveis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bicubo  </span> </p> </td> 
   <td colname="col2"> <p>Seleciona a interpolação bicúbica. Mais intensiva em CPU do que a interpolação bidirecional, mas produz imagens mais nítidas com artefatos de aliasing menos notáveis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> shark2  </span> </p> </td> 
   <td colname="col2"> <p>Seleciona uma função modificada da Janela Lanczos como um algoritmo de interpolação. Pode produzir resultados ligeiramente mais nítidos do que bi-cúbicos a um custo de CPU mais alto. <span class="codeph"> afiado  </span> foi substituído por  <span class="codeph"> afiado2  </span>, que tem uma probabilidade menor de causar artefatos aliasing (Moiré). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharpe  </span> </p> </td> 
   <td colname="col2"> <p>Seleciona o novo amplificador padrão Photoshop para reduzir o tamanho da imagem, que é chamado de "afiador bicúbico" no Adobe Photoshop. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!IMPORTANT]
>
>Para manter a proporção de aspecto de uma imagem ao usar `resMode=bisharp` e `fit=stretch`, é uma prática recomendada usar o parâmetro largura ou o parâmetro altura . Se ambos os parâmetros tiverem de ser definidos, você poderá vinculá-los em uma camada diferente, como mostrado no exemplo a seguir:
>
>`/is/image/is/image/companyname?layer=0&src=is(companyname/imagename?wid=30&hei=30&fit=stretch)&resmode=bisharp`

## Propriedades {#section-a171bacf4ddf43c782e46b86a16d443e}

Atributo da solicitação. Aplica-se a todas as operações de dimensionamento envolvidas na criação da imagem de resposta final, incluindo toda a escala de camadas.

## Padrão {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## Exemplo {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

Recupere uma representação de melhor qualidade de uma imagem em camadas armazenada em um catálogo de imagens. A imagem pode incluir texto. A imagem será processada posteriormente em um aplicativo de edição de imagem e, portanto, solicitará um canal alfa com a imagem.

` http:// *`server`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## Consulte também {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[atributo::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
