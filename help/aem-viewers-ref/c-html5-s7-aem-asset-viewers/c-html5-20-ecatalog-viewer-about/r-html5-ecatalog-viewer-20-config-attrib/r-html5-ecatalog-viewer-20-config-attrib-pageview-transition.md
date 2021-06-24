---
description: PageView.transition
solution: Experience Manager
title: PageView.transition
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo eletrônico
role: Developer,Business Practitioner
exl-id: aa12a210-88d9-4b96-b598-6967496ac668
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---

# PageView.transition{#pageview-transition}

` [PageView.|<containerId>_pageView.]transition= *``*[, *`tempo`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> time</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o tempo em segundos que a animação de uma única ação de zoom leva. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> flexibilização</span></span> </p> </td> 
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

## Propriedades {#section-ebfd9162c8504666bf0e4485bf3b1383}

Opcional.

## Padrão {#section-9f91ce6567384ab691e4d4f8a7015455}

`0.5,0`

## Exemplo {#section-cb6b8793ee9946b8bf1cfddab8612db5}

`transition=2,2`
