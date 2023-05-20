---
description: Ajuste o equilíbrio de cores. Ajusta o valor de cada componente de cor de RGB separadamente.
solution: Experience Manager
title: op_colorbalance
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 93476778-97b0-4ad5-b22a-093239e845f0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# op_colorbalance{#op-colorbalance}

Ajuste o equilíbrio de cores. Ajusta o valor de cada componente de cor de RGB separadamente.

`op_colorbalance= *`redAdj`*, *`greenAdj`*, *`blueAdj`*`

<table id="simpletable_BBDAA6FE9A0E48E3BD8304BDED776713"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> redAdj</span> </p></td> 
  <td class="stentry"> <p>Ajuste do componente vermelho (-100...+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> greenAdj</span> </p></td> 
  <td class="stentry"> <p>Ajuste do componente verde (-100...+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> blueAdj</span> </p></td> 
  <td class="stentry"> <p>Ajuste de componente azul (-100...+100 int). </p></td> 
 </tr> 
</table>

Os dados de imagem de entrada em cinza e CMYK são convertidos em RGB usando conversão nativa, que não é precisa quando o gerenciamento de cores está ativado.

## Propriedades {#section-dff9c934f7c1442bbd02379b688d82e2}

Camada. Se aplica à camada atual ou à imagem composta `layer=comp`. Ignorado pelas camadas de efeito. As imagens e camadas CMYK são convertidas em RGB antes da operação ser aplicada.

## Padrão {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` para nenhuma alteração nas cores.

## Exemplo {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

Empurre o equilíbrio de cores em direção ao vermelho:

… `&op_colorBalance=100,0,0&`…
