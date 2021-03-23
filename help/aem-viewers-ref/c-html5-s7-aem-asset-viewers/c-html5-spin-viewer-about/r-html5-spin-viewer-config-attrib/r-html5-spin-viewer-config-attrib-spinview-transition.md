---
description: SpinView.transition
solution: Experience Manager
title: SpinView.transition
uuid: 9d7ea421-9892-4276-8f22-3e1099f91f2f
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de rotação
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# SpinView.transition{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *``*[, *`tempo`*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> time</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o tempo em segundos que a animação de uma única ação de zoom leva. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> flexibilização</span></span> </p> </td> 
   <td colname="col2"> <p> Cria uma ilusão de aceleração ou desaceleração que faz com que a transição pareça mais natural. Você pode definir o easing para um dos seguintes: </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0 (automático) </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1 (linear) </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2 (quadrático) </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3 (cúbico) </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4 (em quarto) </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5 (quinta) </li> 
     </ul> </p> <p>O modo automático sempre usa transição linear quando o zoom elástico está desativado (padrão). Caso contrário, ele se encaixará em uma das outras funções de atenuação com base no tempo de transição. Ou seja, quanto mais curto for o tempo de transição, mais elevada será a função de atenuação utilizada para acelerar o efeito de aceleração ou desaceleração. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-924163cb2f6542499f49894becef7fb5}

Opcional.

## Padrão {#section-7a2128fd488941948aff18421f533ccf}

`0.5,0`

## Exemplo {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`transition=2,2`
