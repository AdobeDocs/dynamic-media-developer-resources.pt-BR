---
description: Ajuste o equilíbrio de cores. Ajusta o valor de cada componente de cor RGB separadamente.
seo-description: Ajuste o equilíbrio de cores. Ajusta o valor de cada componente de cor RGB separadamente.
seo-title: op_color_balance
solution: Experience Manager
title: op_color_balance
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 177aa6e3-1b32-4254-85f1-d7fe14116e3c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# op_color balance{#op-colorbalance}

Ajuste o equilíbrio de cores. Ajusta o valor de cada componente de cor RGB separadamente.

`op_colorbalance= *``*, *``*, *`redAdjgreenAdjblueAdj`*`

<table id="simpletable_BBDAA6FE9A0E48E3BD8304BDED776713"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> redAdj</span> </p></td> 
  <td class="stentry"> <p>Ajuste de componente vermelho (-100...+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> greenAdj</span> </p></td> 
  <td class="stentry"> <p>Ajuste de componente verde (-100...+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> blueAdj</span> </p></td> 
  <td class="stentry"> <p>Ajuste de componente azul (-100...+100 int). </p></td> 
 </tr> 
</table>

Os dados de imagem de entrada de cinza e CMYK são convertidos em RGB usando conversão ingênua que não é precisa quando o gerenciamento de cores está ativado.

## Propriedades {#section-dff9c934f7c1442bbd02379b688d82e2}

comando Camada. Aplica-se à camada atual ou à imagem composta se `layer=comp`. Ignorado pelas camadas de efeito. As imagens e as camadas CMYK são convertidas em RGB antes da operação ser aplicada.

## Padrão {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` sem alteração de cores.

## Exemplo {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

Empurre o equilíbrio de cores para vermelho:

... `&op_colorBalance=100,0,0&`...
