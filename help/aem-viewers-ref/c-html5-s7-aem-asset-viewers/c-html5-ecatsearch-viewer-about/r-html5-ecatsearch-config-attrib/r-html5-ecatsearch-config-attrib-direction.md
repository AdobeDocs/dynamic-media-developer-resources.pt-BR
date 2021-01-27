---
description: direção
solution: Experience Manager
title: direção
topic: Dynamic Media
uuid: 0a30f3b0-64c8-4799-b4f5-fc8996a8b5a4
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---


# orientation{#direction}

[!DNL `direction=auto|left|right`]

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|esquerda|direita  </span> </p> </td> 
   <td colname="col2"> <p>Especifica a forma como as páginas são exibidas na visualização principal e nas miniaturas. Ela também especifica a forma como o usuário interage com a interface do usuário do visualizador para alterar entre quadros do catálogo. </p> <p>Quando <span class="codeph"> à esquerda </span> é usado, ele define um alinhamento à direita para a página inicial e o alinhamento à esquerda para a última página. Ele costuma subimagens de página individuais para ordem de renderização da esquerda para a direita. Ele também define a visualização principal para usar a animação de slide da direita para a esquerda para avançar no catálogo (no caso de <span class="codeph"> PageView.frametransition </span> estar definida como slide). Finalmente, as miniaturas são definidas para uma ordem de preenchimento da esquerda para a direita. </p> <p>Da mesma forma, quando <span class="codeph"> direita </span> é usado, ele define um alinhamento à esquerda para a página inicial e o alinhamento à direita para a última página. Ele costuma subimagens de página individuais para ordem de renderização da direita para a esquerda. Ele também define a visualização principal para usar a animação de slide da esquerda para a direita para avançar o catálogo (no caso de <span class="codeph"> PageView.frametransition </span> estar definido como slide). Finalmente, ele inverte a ordem das miniaturas para que a visualização das miniaturas seja preenchida na direção direita para esquerda, de cima para baixo. </p> <p>Quando <span class="codeph"> auto </span> estiver definido, o visualizador aplicará o modo <span class="codeph"> direito </span> quando a localidade estiver definida como <span class="codeph"> ja; </span>caso contrário, ele usa o modo <span class="codeph"> esquerdo </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-a66ce10d6c0b449883f654e7e0657e2c}

Opcional.

## Padrão {#section-2879062cee1d4030b43ba3b19693f4f8}

[!DNL `auto`]

## Exemplo {#section-798e4fc8dd9b4b059171b41a608a96ce}

[!DNL `direction=right`]
