---
description: Atributo de configuração para o Visualizador de vídeo interativo.
solution: Experience Manager
title: VideoPlayer.iconeffect
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interativos
role: Developer,Business Practitioner
exl-id: 690dc488-2db0-4166-a308-f1f3438c480a
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 1%

---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

Atributo de configuração para o Visualizador de vídeo interativo.

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Permite que o IconEffect seja exibido na parte superior do vídeo quando ele estiver em pausa. Em alguns dispositivos são usados controles nativos. Nesses casos, o modificador <span class="codeph"> do ícone </span> é ignorado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> count</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o número máximo de vezes em que o IconEffect é exibido e reaparece. Um valor de <span class="codeph"> -1</span> indica que o ícone reaparece indefinidamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> desaparecer</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica a duração da animação show ou hide, em segundos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p> Define o número de segundos em que o IconEffect permanece totalmente visível antes de se ocultar automaticamente. Ou seja, o tempo após o esmaecimento da animação é concluído e antes do início da animação de esmaecimento. Defina como <span class="codeph"> 0</span> para desativar o comportamento de ocultação automática. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
