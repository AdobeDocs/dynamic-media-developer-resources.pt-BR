---
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
title: FlyoutZoomView.flyouttransition
feature: Dynamic Media Classic,Visualizadores,SDK/API,Flyout
role: Developer,Business Practitioner
exl-id: a15723fe-a8be-49c5-bad3-1a1360eeb232
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *``*[, *``*[, *``*[, *`showtimeshowdelayhidetimehidedelay`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> nenhum|slide|desvanecer  </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica o tipo do efeito aplicado quando a exibição do menu suspenso é mostrada ou oculta. Com <span class="codeph"> nenhum </span>, a imagem de flyout aparece instantaneamente quando ativada e pronta; <span class="codeph"> o slide </span> faz com que a animação de slides seja reproduzida na direção esquerda para a direita; <span class="codeph"> o esmaecimento </span> aplica uma transição alfa à imagem do flyout. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime  </span> </span> </p> </td> 
   <td colname="col2"> <p> Número de segundos que a animação de exibição leva para ser concluída. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showdelay  </span> </span> </p> </td> 
   <td colname="col2"> <p> O atraso em segundos entre a ação do usuário que inicia a animação show e o início da própria animação show. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> horário  </span> </span> </p> </td> 
   <td colname="col2"> <p> Número de segundos que a animação de ocultação leva para ser concluída. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> oculto  </span> </span> </p> </td> 
   <td colname="col2"> <p> O atraso em segundos entre a ação do usuário que inicia a animação de ocultação e o início da própria animação de ocultação. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Padrão {#section-a08032f0fcf041c09e63c0238a339fc9}

`fade,1,0,1,0`

## Exemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`flyouttransition=slide,1,1,2,1`
