---
title: SmartCropVideoPlayer.iconeffect
description: Atributo de configuração para o Visualizador de Corte inteligente de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 369e389c-f0e2-405e-b4aa-2f6b9ac8b8ea
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# SmartCropVideoPlayer.iconeffect{#smartcropvideoplayer-iconeffect}

Atributo de configuração para o Visualizador de Corte inteligente de vídeo.

` [SmartCropVideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *`count`*][, *`fade`*][, *`autoHide`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> Ativa o IconEffect para ser exibido na parte superior do vídeo quando ele for pausado. Em alguns dispositivos, os controles nativos são usados. Nesse caso, o modificador <span class="codeph"> iconeffect</span> é ignorado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> contagem</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica o número máximo de vezes que o IconEffect aparece e reaparece. Um valor de <span class="codeph"> -1</span> indica que o ícone reaparece indefinidamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fade</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica a duração da animação de exibição ou ocultação, em segundos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p> Define o número de segundos que o IconEffect permanece visível antes de ser ocultado automaticamente. Ou seja, o tempo após a conclusão da animação de aparecimento e antes do início da animação de desaparecimento. Uma configuração de <span class="codeph"> 0</span> desabilita o comportamento de ocultação automática. </p> </td> 
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
