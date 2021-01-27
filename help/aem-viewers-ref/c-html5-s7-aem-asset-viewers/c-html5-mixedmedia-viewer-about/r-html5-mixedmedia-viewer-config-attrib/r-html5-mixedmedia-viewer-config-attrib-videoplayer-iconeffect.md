---
description: VideoPlayer.iconeffect
solution: Experience Manager
title: VideoPlayer.iconeffect
topic: Dynamic Media
uuid: 8e112f3c-8fa6-4c77-94c5-5027275225e7
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 1%

---


# VideoPlayer.iconeffect{#videoplayer-iconeffect}

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_38995A95977645AD8716203987DD9909"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> Permite que IconEffect seja exibido na parte superior do vídeo quando o vídeo estiver pausado. Em alguns dispositivos, controles nativos são usados. Nesse caso, o modificador do ícone <span class="codeph"></span> é ignorado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica o número máximo de vezes que IconEffect é exibido e reexibido. Um valor de <span class="codeph"> -1</span> indica que o ícone reaparece indefinidamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> desvanecer</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica a duração de mostrar ou ocultar animação, em segundos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p> Define o número de segundos em que o IconEffect permanece visível antes de se ocultar automaticamente. Ou seja, o tempo após a animação de desaparecimento gradual é concluído e antes dos start de animação de desaparecimento gradual. Uma configuração de <span class="codeph"> 0</span> desativa o comportamento de ocultação automática. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,-1,0.3,0`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
