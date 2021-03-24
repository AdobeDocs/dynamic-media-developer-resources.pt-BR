---
description: Atributo de configuração para o Visualizador de vídeo interativo.
solution: Experience Manager
title: VideoPlayer.playback
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interativos
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# VideoPlayer.playback{#videoplayer-playback}

Atributo de configuração para o Visualizador de vídeo interativo.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressivo</span> </p> </td> 
   <td colname="col2"> <p> Define o tipo de reprodução usado pelo visualizador. </p> <p>Quando <span class="codeph"> auto</span> é definido, na maioria dos navegadores de desktop e em todos os dispositivos iOS, o visualizador usa vídeo de transmissão HTML5 no formato HLS e volta para a reprodução HTML5 progressiva em determinados sistemas como o Internet Explorer e o Android mais antigos. </p> <p>Quando <span class="codeph"> progressivo</span> é definido, o visualizador depende apenas da reprodução HTML5, como nativamente compatível pelos navegadores, e reproduz vídeo progressivamente em todos os sistemas. </p> <p>Para obter mais informações sobre a seleção de reprodução nos modos nativos <span class="codeph"> auto</span> e <span class="codeph"> progressivo</span>, consulte o Guia do Usuário do SDK de Visualizadores HTML5. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`auto`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
