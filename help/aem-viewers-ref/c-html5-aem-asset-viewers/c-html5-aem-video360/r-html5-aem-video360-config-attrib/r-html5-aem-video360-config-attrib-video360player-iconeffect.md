---
description: Atributo de configuração para o visualizador do Video360.
solution: Experience Manager
title: Video360Player.iconeffect
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo 360 VR
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 4%

---


# Video360Player.iconeffect{#video-player-iconeffect}

Atributo de configuração para o visualizador do Video360.

` [Video360Player.|<containerId>_video360Player.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

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
