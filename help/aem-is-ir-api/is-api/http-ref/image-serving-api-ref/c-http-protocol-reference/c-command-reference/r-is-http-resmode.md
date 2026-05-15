---
title: resMode
description: Modo de reamostragem. Escolha o algoritmo de reamostragem e/ou interpolação a ser usado para dimensionar dados de imagem. Também se aplica à rotação de camadas de texto e ao redimensionamento de imagens compostas durante a transformação de exibição.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 63c1c028-0378-4a38-8018-e358491786d8
TQID: 'https://experienceleague.adobe.com/uT9SBMqQ0JvU-S8BF2y0kY6C--jNhvggbRwhTpTJOGg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 269
ht-degree: 0%

---

# resMode{#resmode}

Modo de reamostragem. Escolha o algoritmo de reamostragem e/ou interpolação a ser usado para dimensionar dados de imagem. Também se aplica à rotação de camadas de texto e ao redimensionamento de imagens compostas durante a transformação de exibição.

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bilhão </span> </p> </td> 
   <td colname="col2"> <p>Seleciona a interpolação bilinear padrão. Método de reamostragem mais rápido; alguns artefatos de suavização são visíveis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>Seleciona a interpolação bi-cúbica. Mais intensa de CPU do que a interpolação bi-linear, mas produz imagens mais nítidas com menos artefatos de suavização visíveis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>Seleciona uma função de janela Lanczos modificada como um algoritmo de interpolação. Pode produzir resultados ligeiramente mais nítidos do que o bi-cúbico a um custo de CPU mais alto. <span class="codeph"> sharp </span> foi substituído por <span class="codeph"> sharp2 </span>, que tem uma probabilidade menor de causar artefatos de suavização (Moiré). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharp </span> </p> </td> 
   <td colname="col2"> <p>Seleciona o reamostragem padrão do Photoshop para reduzir o tamanho da imagem, chamado de "bicúbico mais nítido" no Adobe Photoshop. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!IMPORTANT]
>
>Para manter a proporção de uma imagem ao usar `resMode=bisharp` e `fit=stretch`, é prática recomendada usar o parâmetro largura ou o parâmetro altura. Se ambos os parâmetros tiverem de ser definidos, você poderá envolvê-los em uma camada diferente, conforme mostrado no exemplo a seguir:
>
>`/is/image/is/image/companyname?layer=0&src=is(companyname/imagename?wid=30&hei=30&fit=stretch)&resmode=bisharp`

## Propriedades {#section-a171bacf4ddf43c782e46b86a16d443e}

Solicitar atributo. Aplica-se a todas as operações de dimensionamento envolvidas na criação da imagem de resposta final, incluindo o dimensionamento de todas as camadas.

## Padrão {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## Exemplo {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

Recupere uma representação de melhor qualidade de uma imagem em camadas armazenada em um catálogo de imagens. A imagem pode incluir texto. A imagem é processada em um aplicativo de edição de imagens e, portanto, solicita um canal alfa com a imagem.

` http:// *`servidor`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## Consulte também {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[attribute::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
