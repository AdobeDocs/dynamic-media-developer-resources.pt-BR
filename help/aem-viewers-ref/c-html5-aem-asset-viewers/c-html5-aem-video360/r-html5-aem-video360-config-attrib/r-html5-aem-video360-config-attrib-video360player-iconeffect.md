---
title: Video360Player.iconeffect
description: Atributo de configuração para o Video360 Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 818ea14b-4dab-4447-9645-46f2ba82547b
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---

# Video360Player.iconeffect{#video-player-iconeffect}

Atributo de configuração para o Video360 Viewer.

` [Video360Player.|<containerId>_video360Player.]iconeffect=0|1[, *`count`*][, *`fade`*][, *`autoHide`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Permite que o IconEffect seja exibido na parte superior do vídeo quando ele estiver no estado pausado. Em alguns dispositivos, os controles nativos são usados. Nesses casos, a <span class="codeph">iconeffect</span> o modificador é ignorado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> count</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o número máximo de vezes que o IconEffect aparece e reaparece. Um valor de <span class="codeph"> -1</span> indica que o ícone reaparece indefinidamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> fade</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica a duração da animação de exibição ou ocultação, em segundos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p> Define o número de segundos que o IconEffect permanece totalmente visível antes de ser ocultado automaticamente. Ou seja, o tempo depois que a animação de aparecimento e desaparecimento gradual é concluída e antes que a animação de desaparecimento gradual seja iniciada. Defina como <span class="codeph"> 0</span> para desativar o comportamento de ocultação automática. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
