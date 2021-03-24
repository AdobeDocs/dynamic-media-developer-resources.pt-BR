---
description: direção
solution: Experience Manager
title: direção
feature: Dynamic Media Classic,Visualizadores,SDK/API,Pesquisa de catálogo eletrônico
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---


# direção{#direction}

[!DNL `direction=auto|left|right`]

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|esquerda|direita  </span> </p> </td> 
   <td colname="col2"> <p>Especifica a maneira como as páginas são exibidas na exibição principal e nas miniaturas. Especifica também a forma como o usuário interage com a interface do usuário do visualizador para alterar entre quadros de catálogo. </p> <p>Quando <span class="codeph"> à esquerda </span> é usado, ele define um alinhamento à direita para a página inicial e o alinhamento à esquerda para a última página. Ele une subimagens de páginas individuais para a ordem de renderização da esquerda para a direita. Também define a exibição principal para usar a animação de slide da direita para a esquerda para avançar o catálogo (caso <span class="codeph"> PageView.framework transition </span> esteja definida como slide). Finalmente, as miniaturas são definidas para uma ordem de preenchimento da esquerda para a direita. </p> <p>Da mesma forma, quando <span class="codeph"> direita </span> é usado, ele define um alinhamento à esquerda para a página inicial e ao lado direito para a última página. Ele une subimagens de página individuais para ordem de renderização da direita para a esquerda. Também define a exibição principal para usar a animação de slide da esquerda para a direita para avançar o catálogo (caso <span class="codeph"> PageView.framework transition </span> esteja definida como slide). Por fim, ele inverte a ordem das miniaturas para que a exibição de miniaturas seja preenchida na direção direita para a esquerda, de cima para baixo. </p> <p>Quando <span class="codeph"> auto </span> está definido, o visualizador aplica o modo <span class="codeph"> direito </span> quando a localidade está definida como <span class="codeph"> ja; </span>caso contrário, ele usará o modo <span class="codeph"> esquerdo </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-a66ce10d6c0b449883f654e7e0657e2c}

Opcional.

## Padrão {#section-2879062cee1d4030b43ba3b19693f4f8}

[!DNL `auto`]

## Exemplo {#section-798e4fc8dd9b4b059171b41a608a96ce}

[!DNL `direction=right`]
