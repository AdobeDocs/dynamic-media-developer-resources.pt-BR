---
title: VideoPlayer.playback
description: Atributo de configuração para o Visualizador de vídeo interativo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: fa49e025-1a46-4be7-ad1e-eda3b31bdc8d
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---

# VideoPlayer.playback{#videoplayer-playback}

Atributo de configuração para o Visualizador de vídeo interativo.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> Define o tipo de reprodução usado pelo visualizador. </p> <p>Quando <span class="codeph"> automático</span> estiver definido, na maioria dos navegadores de desktop e em todos os dispositivos iOS, o visualizador usa o vídeo de transmissão HTML5 no formato HLS. E ele se baseia na reprodução progressiva do HTML5 em determinados sistemas, como o Internet Explorer e o Android™ mais antigos. </p> <p>Quando <span class="codeph"> progressivo</span> estiver definido, o visualizador dependerá somente da reprodução do HTML5, como nativamente suportado pelos navegadores, e reproduzirá o vídeo progressivamente em todos os sistemas. </p> <p>Para obter mais informações sobre a seleção de reprodução em <span class="codeph"> automático</span> e <span class="codeph"> progressivo</span> modos nativos, consulte o Guia do usuário do SDK de visualizadores do HTML5. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`auto`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
