---
title: PageView.frametransition
description: PageView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026c2fc5-0460-481c-aca9-ddd25371779c
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# PageView.frametransition{#pageview-frametransition}

` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`duração`*]`

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide|turno|automático</span> </p> </td> 
   <td colname="col2"> <p> Especifica o tipo de efeito aplicado na alteração do quadro. </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> slide</span> ativa uma transição em que o quadro antigo desaparece e o novo quadro surge para exibi-lo. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p>O <span class="codeph"> turn</span> habilita um efeito de virar página, quando um usuário pode arrastar um dos quatro cantos espelhados e executar um giro de página interativo. </p> <p>Quando <span class="codeph"> turn</span> é usado, a aparência do componente é controlada com o modificador <span class="codeph"> pageturnstyle</span> e a classe CSS <span class="codeph"> .s7pagedivider</span> é ignorada. </p> <p>Nota:  <p>A animação <span class="codeph"> turn</span> não tem suporte no Motorola Xoom. </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> auto</span> define a transição de ativação em sistemas desktop e a transição de slides em dispositivos de toque. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duração</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica a duração em segundos de um efeito de transição <span class="codeph"> slide</span> ou <span class="codeph"> turn</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-4d25a3f483834d2b9586fa70270ce6bd}

Opcional.

## Padrão {#section-d677f04f1c894966884ce9d77a5ea1c1}

`slide,0.3`

## Exemplo {#section-b877011e5f6240718e9451be8f622c02}

`frametransition=auto,1`
