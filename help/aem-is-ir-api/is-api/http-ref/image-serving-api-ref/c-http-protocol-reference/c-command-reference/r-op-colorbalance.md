---
description: Ajuste o equilíbrio de cores. Ajusta o valor de cada componente de cor RGB separadamente.
solution: Experience Manager
title: op_color_balance
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# op_colorbalance{#op-colorbalance}

Ajuste o equilíbrio de cores. Ajusta o valor de cada componente de cor RGB separadamente.

`op_colorbalance= *``*, *``*, *`redAdjgreenAdjblueAdj`*`

<table id="simpletable_BBDAA6FE9A0E48E3BD8304BDED776713"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> redAdj</span> </p></td> 
  <td class="stentry"> <p>Ajuste do componente vermelho (-100...+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> greenAdj</span> </p></td> 
  <td class="stentry"> <p>Ajuste de componente verde (-100...+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> blueAdj</span> </p></td> 
  <td class="stentry"> <p>Ajuste do componente azul (-100...+100 int). </p></td> 
 </tr> 
</table>

Os dados de imagens de entrada de cinza e CMYK são convertidos em RGB usando conversão nativa que não é precisa quando o gerenciamento de cores está ativado.

## Propriedades {#section-dff9c934f7c1442bbd02379b688d82e2}

comando Camada. Aplica-se à camada atual ou à imagem composta se `layer=comp`. Ignorado por camadas de efeito. Imagens e camadas CMYK são convertidas em RGB antes da aplicação da operação.

## Padrão {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` sem alteração de cores.

## Exemplo {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

Empurre o equilíbrio de cores em direção ao vermelho:

... `&op_colorBalance=100,0,0&`...
