---
title: SpinView.transition
description: SpinView.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: fcffe282-65a5-4093-8838-71a64085b387
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---

# SpinView.transition{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *`hora`*[, *`atenuação`*]`

<table id="table_5B8094216AE94DC59671E06DB941A366"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> vez</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o tempo em segundos que leva a animação de uma única ação de etapa de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> atenuação</span></span> </p> </td> 
   <td colname="col2"> <p> Cria uma ilusão de aceleração ou desaceleração que faz a transição parecer mais natural. Você pode definir a atenuação como uma das seguintes opções: </p> <p> 
     <ul id="ul_7B9694978D96449AB986AED1CF7F649D"> 
      <li id="li_904CEC8AD5834139A5585EE70ACE9C80">0 (automático) </li> 
      <li id="li_471D4CD39C10415497B1714B0AD961B9"> 1 (linear) </li> 
      <li id="li_7A0F9F1186604E75BAA19626A844236A"> 2 (quadrático) </li> 
      <li id="li_B8D4C40D795642AB835925582B707158"> 3 (cúbico) </li> 
      <li id="li_2B9F7324BB89455C89C1CAE1BD5BBB65"> 4 (quartic) </li> 
      <li id="li_B94A553B6E844247BE88ECA0A8CEB811"> 5 (quintico) </li> 
     </ul> </p> <p>O modo Automático sempre usa a transição linear quando o zoom elástico está desativado (padrão). Caso contrário, ele se encaixa em uma das outras funções de atenuação com base no tempo de transição. Isto é, quanto menor o tempo de transição, maior a função de atenuação é usada para acelerar o efeito de aceleração ou desaceleração. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0.5,0`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=2,2`
