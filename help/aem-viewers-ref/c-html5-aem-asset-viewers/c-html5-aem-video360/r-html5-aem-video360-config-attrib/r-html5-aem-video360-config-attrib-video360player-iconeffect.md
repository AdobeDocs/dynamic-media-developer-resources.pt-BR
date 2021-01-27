---
description: Atributo de configuração para o visualizador Video360.
seo-description: Atributo de configuração para o visualizador Video360.
seo-title: Video360Player.iconeffect
solution: Experience Manager
title: Video360Player.iconeffect
topic: Dynamic Media
uuid: a0a2f840-e330-4636-8daf-1cd3f2eddf01
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 5%

---


# Video360Player.iconeffect{#video-player-iconeffect}

Atributo de configuração para o visualizador Video360.

` [Video360Player.|<containerId>_video360Player.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Permite que IconEffect seja exibido na parte superior do vídeo quando o vídeo estiver em estado de pausa. Em alguns dispositivos, controles nativos são usados. Nesses casos, o modificador do ícone <span class="codeph"></span> é ignorado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> count</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o número máximo de vezes que IconEffect é exibido e reexibido. Um valor de <span class="codeph"> -1</span> indica que o ícone reaparece indefinidamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> desvanecer</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica a duração de mostrar ou ocultar animação, em segundos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p> Define o número de segundos em que o IconEffect permanece totalmente visível antes de se ocultar automaticamente. Ou seja, o tempo após o desaparecimento gradual da animação é concluído e antes dos start de animação serem apagados. Defina como <span class="codeph"> 0</span> para desativar o comportamento de ocultação automática. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
