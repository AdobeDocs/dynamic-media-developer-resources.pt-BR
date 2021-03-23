---
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
title: FlyoutZoomView.flyouttransition
uuid: 0b94956d-9ee6-409e-9b52-29c888932a0e
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom em linha
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '130'
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

## Propriedades {#section-e6310c8c4e8547689a5b48ceddb3671d}

Opcional.

## Padrão {#section-fcb06fd8e7e945e590094efcf9a1d510}

`fade,1,0,1,0`

## Exemplo {#section-3a188ab955c445bcb2efa3c49722c10d}

`flyouttransition=slide,1,1,2,1`
