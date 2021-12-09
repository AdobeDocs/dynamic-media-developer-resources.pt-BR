---
title: direção
description: Especifica a maneira como as páginas são exibidas na exibição principal e nas miniaturas. Especifica também a forma como o usuário interage com a interface do usuário do visualizador para alterar entre quadros de catálogo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7d3df37-3e8b-438f-8b24-035b6982dc14
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# direção{#direction}

`direction=auto|left|right`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|esquerda|direita </span> </p> </td> 
   <td colname="col2"> <p>Especifica a maneira como as páginas são exibidas na exibição principal e nas miniaturas. Especifica também a forma como o usuário interage com a interface do usuário do visualizador para alterar entre quadros de catálogo. </p> <p>When <span class="codeph"> left </span> é usada, ela define um alinhamento à direita para a página inicial e o alinhamento à esquerda para a última página. Ele une subimagens de páginas individuais para a ordem de renderização da esquerda para a direita. Também define a exibição principal para usar a animação de slide da direita para a esquerda para avançar o catálogo (no caso <span class="codeph"> Transição PageView.framework </span> está definida como slide). Finalmente, as miniaturas são definidas para uma ordem de preenchimento da esquerda para a direita. </p> <p>Da mesma forma, quando <span class="codeph"> right </span> é usada para definir um alinhamento à esquerda para a página inicial e ao lado direito para a última página. Ele une subimagens de página individuais para ordem de renderização da direita para a esquerda. Também define a exibição principal para usar a animação de slide da esquerda para a direita para avançar o catálogo (no caso <span class="codeph"> Transição PageView.framework </span> está definida como slide). Por fim, ele inverte a ordem das miniaturas para que a exibição de miniaturas seja preenchida na direção direita para a esquerda, de cima para baixo. </p> <p>When <span class="codeph"> auto </span> estiver definido, o visualizador será aplicado <span class="codeph"> right </span> modo quando a localidade está definida como <span class="codeph"> ja; </span>caso contrário, ele usará <span class="codeph"> left </span> modo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-a66ce10d6c0b449883f654e7e0657e2c}

Opcional.

## Padrão {#section-2879062cee1d4030b43ba3b19693f4f8}

`auto`

## Exemplo {#section-798e4fc8dd9b4b059171b41a608a96ce}

`direction=right`
