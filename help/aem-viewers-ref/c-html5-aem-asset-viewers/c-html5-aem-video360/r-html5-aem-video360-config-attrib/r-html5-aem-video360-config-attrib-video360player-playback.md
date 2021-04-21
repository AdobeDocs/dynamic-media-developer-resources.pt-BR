---
description: Atributo de configuração para o visualizador do Video360.
solution: Experience Manager
title: Video360Player.playback
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,Business Practitioner
exl-id: e5a56195-c3ca-4748-aef6-e1f143ac254d
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 3%

---

# Video360Player.playback{#video-player-playback}

Atributo de configuração para o visualizador do Video360.

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressivo</span> </p> </td> 
   <td colname="col2"> <p> Define o tipo de reprodução usado pelo visualizador. </p> <p>Quando <span class="codeph"> auto</span> é definido, na maioria dos navegadores de desktop e em todos os dispositivos iOS, o visualizador usa vídeo de transmissão HTML5 no formato HLS e volta para a reprodução HTML5 progressiva em determinados sistemas como o Internet Explorer e o Android mais antigos. </p> <p>Quando <span class="codeph"> progressivo</span> é definido, o visualizador depende apenas da reprodução HTML5, como nativamente compatível pelos navegadores, e reproduz vídeo progressivamente em todos os sistemas. </p> <p>Para obter mais informações sobre a seleção de reprodução nos modos nativos <span class="codeph"> auto</span> e <span class="codeph"> progressivo</span>, consulte o Guia do Usuário do SDK de Visualizadores HTML5. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional. Ignorado quando o visualizador funciona com vídeo externo.

Consulte [Suporte a vídeo externo](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) para obter detalhes.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`auto`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
