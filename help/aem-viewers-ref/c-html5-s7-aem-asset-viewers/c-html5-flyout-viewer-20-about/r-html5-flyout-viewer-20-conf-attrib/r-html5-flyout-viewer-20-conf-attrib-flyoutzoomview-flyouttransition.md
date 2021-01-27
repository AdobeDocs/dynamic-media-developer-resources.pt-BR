---
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
title: FlyoutZoomView.flyouttransition
topic: Dynamic Media
uuid: f1a9f2bc-9a13-4980-9241-e835a0aadd2c
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *``*[, *``*[, *``*[, *`showtimeshowdelayhidetimehidedelay`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> nenhum|slide|esmaecer  </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica o tipo do efeito aplicado quando a visualização flyout é mostrada ou oculta. Com <span class="codeph"> nenhum </span>, a imagem flyout aparece instantaneamente quando ativada e pronta; <span class="codeph"> o slide </span> faz com que a animação do slide seja reproduzida na direção da esquerda para a direita; <span class="codeph"> fade </span> aplica uma transição alfa à imagem flyout. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hora  </span> </span> </p> </td> 
   <td colname="col2"> <p> Número de segundos que a animação de ocultação leva para ser concluída. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> esconderijo  </span> </span> </p> </td> 
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
