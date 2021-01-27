---
description: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
topic: Dynamic Media
uuid: 12595a89-bad5-4224-aeff-52ce6bb615ee
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# PageView.frametransition{#pageview-frametransition}

[!DNL ` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`duração`*]`]

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide|girar|automático</span> </p> </td> 
   <td colname="col2"> <p> Especifica o tipo de efeito aplicado na alteração de quadro. </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> O </span> slide ativa uma transição na qual o quadro antigo desliza para fora da visualização e o novo quadro desliza para dentro da visualização. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> ativa </span> um efeito de giro de página, quando um usuário pode arrastar um dos quatro cantos espelhados e executar um giro de página interativo. </p> <p>Quando <span class="codeph"> Turn</span> é usado, a aparência do componente é controlada pelo modificador <span class="codeph"> pageturnstyle</span> e a classe <span class="codeph"> .s7pagediv</span> CSS é ignorada. </p> <p>Observação:  <p><span class="codeph"> A </span> animação não é suportada no Motorola Xoom. </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> define </span> automaticamente a transição de giro nos sistemas de desktop e a transição do slide nos dispositivos de toque. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duração</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica a duração em segundos de um efeito de transição <span class="codeph"> slide</span> ou <span class="codeph"> de virar</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-4d25a3f483834d2b9586fa70270ce6bd}

Opcional.

## Padrão {#section-d677f04f1c894966884ce9d77a5ea1c1}

[!DNL `slide,0.3`]

## Exemplo {#section-b877011e5f6240718e9451be8f622c02}

[!DNL `frametransition=auto,1`]
