---
description: SpinView.transition
solution: Experience Manager
title: SpinView.transition
uuid: d5cc319a-fb0b-41d3-a118-f00376a127e4
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídias mistas
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---


# SpinView.transition{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *``*[, *`tempo`*]`

<table id="table_5B8094216AE94DC59671E06DB941A366"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> time</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o tempo em segundos que a animação de uma única ação de zoom leva. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> flexibilização</span></span> </p> </td> 
   <td colname="col2"> <p> Cria uma ilusão de aceleração ou desaceleração que faz com que a transição pareça mais natural. Você pode definir o easing para um dos seguintes: </p> <p> 
     <ul id="ul_7B9694978D96449AB986AED1CF7F649D"> 
      <li id="li_904CEC8AD5834139A5585EE70ACE9C80">0 (automático) </li> 
      <li id="li_471D4CD39C10415497B1714B0AD961B9"> 1 (linear) </li> 
      <li id="li_7A0F9F1186604E75BAA19626A844236A"> 2 (quadrático) </li> 
      <li id="li_B8D4C40D795642AB835925582B707158"> 3 (cúbico) </li> 
      <li id="li_2B9F7324BB89455C89C1CAE1BD5BBB65"> 4 (em quarto) </li> 
      <li id="li_B94A553B6E844247BE88ECA0A8CEB811"> 5 (quinta) </li> 
     </ul> </p> <p>O modo automático sempre usa transição linear quando o zoom elástico está desativado (padrão). Caso contrário, ele se encaixará em uma das outras funções de atenuação com base no tempo de transição. Ou seja, quanto mais curto for o tempo de transição, mais elevada será a função de atenuação utilizada para acelerar o efeito de aceleração ou desaceleração. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0.5,0`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=2,2`
