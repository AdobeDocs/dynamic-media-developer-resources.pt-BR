---
title: PageView.transition
description: PageView.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: aa12a210-88d9-4b96-b598-6967496ac668
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---

# PageView.transition{#pageview-transition}

` [PageView.|<containerId>_pageView.]transition= *`hora`*[, *`atenuação`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> hora</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o tempo em segundos que leva a animação de uma única ação de etapa de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> atenuação</span></span> </p> </td> 
   <td colname="col2"> <p> Cria uma ilusão de aceleração ou desaceleração que faz a transição parecer mais natural. Você pode definir a atenuação como uma das seguintes opções: </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0 (automático) </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1 (linear) </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2 (quadrático) </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3 (cúbico) </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4 (quartic) </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5 (quintico) </li> 
     </ul> </p> <p>O modo Automático sempre usa a transição linear quando o zoom elástico está desativado (padrão). Caso contrário, ele se encaixa em uma das outras funções de atenuação com base no tempo de transição. Isto é, quanto menor o tempo de transição, maior a função de atenuação é usada para acelerar o efeito de aceleração ou desaceleração. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-ebfd9162c8504666bf0e4485bf3b1383}

Opcional.

## Padrão {#section-9f91ce6567384ab691e4d4f8a7015455}

`0.5,0`

## Exemplo {#section-cb6b8793ee9946b8bf1cfddab8612db5}

`transition=2,2`
