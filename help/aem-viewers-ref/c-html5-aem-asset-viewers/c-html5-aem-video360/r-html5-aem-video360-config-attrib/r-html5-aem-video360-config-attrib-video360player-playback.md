---
title: Video360Player.playback
description: Atributo de configuração para o Video360 Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: e5a56195-c3ca-4748-aef6-e1f143ac254d
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# Video360Player.playback{#video-player-playback}

Atributo de configuração para o Video360 Viewer.

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> Define o tipo de reprodução usado pelo visualizador. </p> <p>Quando <span class="codeph"> automático</span> estiver definido, na maioria dos navegadores de desktop e em todos os dispositivos iOS, o visualizador usa o vídeo de transmissão HTML5 no formato HLS. E ele se baseia na reprodução progressiva do HTML5 em determinados sistemas, como o Internet Explorer e o Android™ mais antigos. </p> <p>Quando <span class="codeph"> progressivo</span> estiver definido, o visualizador dependerá somente da reprodução do HTML5, como nativamente suportado pelos navegadores, e reproduzirá o vídeo progressivamente em todos os sistemas. </p> <p>Para obter mais informações sobre a seleção de reprodução em <span class="codeph"> automático</span> e <span class="codeph"> progressivo</span> modos nativos, consulte o Guia do usuário do SDK de visualizadores do HTML5. </p> </td> 
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
