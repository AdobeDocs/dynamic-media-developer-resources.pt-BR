---
description: Atributo de configuração para o Visualizador de vídeo.
solution: Experience Manager
title: VideoPlayer.iconeffect
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 1%

---


# VideoPlayer.iconeffect{#videoplayer-iconeffect}

Atributo de configuração para o Visualizador de vídeo.

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> Permite que o IconEffect seja exibido na parte superior do vídeo quando o vídeo é pausado. Em alguns dispositivos são usados controles nativos. Nesse caso, o modificador do ícone <span class="codeph"></span> é ignorado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica o número máximo de vezes em que o IconEffect é exibido e reaparece. Um valor de <span class="codeph"> -1</span> indica que o ícone reaparece indefinidamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> desaparecer</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica a duração da animação show ou hide, em segundos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p> Define o número de segundos em que o IconEffect permanece visível antes de se ocultar automaticamente. Ou seja, o tempo após a animação de esmaecimento é concluída e antes do início da animação de esmaecimento. Uma configuração de <span class="codeph"> 0</span> desativa o comportamento de ocultação automática. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`1,-1,0.3,0`

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
iconeffect=0
```

