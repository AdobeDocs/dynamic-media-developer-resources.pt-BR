---
title: direção
description: direção
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 0f78a835-9057-4c79-843a-52b33a1bdd3f
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# direção{#direction}

[!DNL `direction=auto|left|right`]

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p>Especifica como as páginas são exibidas na exibição principal e nas miniaturas. Também especifica a forma como o usuário interage com a interface do usuário do visualizador para alterar entre quadros do catálogo. </p> <p>Quando <span class="codeph"> esquerda </span> é usado, ele define um alinhamento à direita para a página inicial e um alinhamento à esquerda para a última página. Ele une subimagens de página individuais para a ordem de renderização da esquerda para a direita. Ele também define o modo de exibição principal para usar a animação de slides da direita para a esquerda para avançar o catálogo (caso <span class="codeph"> PageView.frametransition </span> esteja definido como slide). Finalmente, as miniaturas são definidas para uma ordem de preenchimento da esquerda para a direita. </p> <p>Da mesma forma, quando <span class="codeph"> direita </span> é usado, ele define um alinhamento à esquerda para a página inicial e um alinhamento à direita para a última página. Ele une subimagens de página individuais para a ordem de renderização da direita para a esquerda. Ele também define o modo de exibição principal para usar a animação de slides da esquerda para a direita para avançar o catálogo (caso <span class="codeph"> PageView.frametransition </span> esteja definido como slide). Por fim, inverte a ordem das miniaturas para que a visualização das miniaturas seja preenchida da direita para a esquerda, de cima para baixo. </p> <p>Quando <span class="codeph"> auto </span> está definido, o visualizador aplica o modo <span class="codeph"> right </span> quando a localidade está definida como <span class="codeph"> ja; </span>caso contrário, ele usa o modo <span class="codeph"> left </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-a66ce10d6c0b449883f654e7e0657e2c}

Opcional.

## Padrão {#section-2879062cee1d4030b43ba3b19693f4f8}

[!DNL `auto`]

## Exemplo {#section-798e4fc8dd9b4b059171b41a608a96ce}

[!DNL `direction=right`]
