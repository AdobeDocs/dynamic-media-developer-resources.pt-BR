---
title: op_colorbalance
description: Ajuste o equilíbrio de cores. Ajusta o valor de cada componente de cor do RGB separadamente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 93476778-97b0-4ad5-b22a-093239e845f0
TQID: 'https://experienceleague.adobe.com/etLnTD-hMe5kOnvak7n47O0XwOWvqtC5av4FkYZpaGI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 114
ht-degree: 0%

---

# op_colorbalance{#op-colorbalance}

Ajuste o equilíbrio de cores. Ajusta o valor de cada componente de cor do RGB separadamente.

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

Camada. Aplica-se à camada atual ou à imagem composta, se `layer=comp`. Ignorado pelas camadas de efeito. As imagens e camadas CMYK são convertidas em RGB antes da operação ser aplicada.

## Padrão {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` para nenhuma alteração nas cores.

## Exemplo {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

Empurre o equilíbrio de cores em direção ao vermelho:

... `&op_colorBalance=100,0,0&`...
