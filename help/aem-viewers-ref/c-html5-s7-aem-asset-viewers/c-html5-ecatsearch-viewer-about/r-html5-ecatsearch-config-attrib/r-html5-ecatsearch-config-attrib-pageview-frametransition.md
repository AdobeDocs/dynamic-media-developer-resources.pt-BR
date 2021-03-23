---
description: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
uuid: 12595a89-bad5-4224-aeff-52ce6bb615ee
feature: Dynamic Media Classic,Visualizadores,SDK/API,Pesquisa de catálogo eletrônico
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# PageView.frametransition{#pageview-frametransition}

[!DNL ` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`duration`*]`]

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide|rodar|automático</span> </p> </td> 
   <td colname="col2"> <p> Especifica o tipo de efeito que é aplicado na alteração de quadro. </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> O </span> slide ativa uma transição em que o quadro antigo desliza para fora da exibição e os novos slides do quadro para exibir. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> </span> ativa um efeito de virar página, quando um usuário pode arrastar um dos quatro cantos de disseminação e executar um flip de página interativo. </p> <p>Quando <span class="codeph"> Turn</span> é usado, a aparência do componente é controlada com o modificador <span class="codeph"> pageturnstyle</span> e a classe CSS <span class="codeph"> .s7pagedivider</span> é ignorada. </p> <p>Observação:  <p><span class="codeph"> </span> a animação não é compatível com o Motorola Xoom. </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> O </span> define automaticamente a transição de giro em sistemas de desktop e a transição de slide em dispositivos de toque. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duration</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica a duração em segundos de um efeito de transição <span class="codeph"> slide</span> ou <span class="codeph"> girar</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-4d25a3f483834d2b9586fa70270ce6bd}

Opcional.

## Padrão {#section-d677f04f1c894966884ce9d77a5ea1c1}

[!DNL `slide,0.3`]

## Exemplo {#section-b877011e5f6240718e9451be8f622c02}

[!DNL `frametransition=auto,1`]
