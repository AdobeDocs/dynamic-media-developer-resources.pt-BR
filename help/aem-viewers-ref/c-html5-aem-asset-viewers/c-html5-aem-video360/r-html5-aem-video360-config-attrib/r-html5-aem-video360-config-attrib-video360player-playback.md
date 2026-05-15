---
title: Video360Player.playback
description: Atributo de configuração para o Video360 Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: e5a56195-c3ca-4748-aef6-e1f143ac254d
TQID: 'https://experienceleague.adobe.com/2Q41XrgRhpCJXlpHtdIVJkcy2eqVNTK4lSo023yPRoI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 122
ht-degree: 0%

---

# Video360Player.playback{#video-player-playback}

Atributo de configuração para o Video360 Viewer.

`[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> Define o tipo de reprodução usado pelo visualizador. </p> <p>Quando <span class="codeph"> auto</span> está definido, na maioria dos navegadores de desktop e em todos os dispositivos iOS, o visualizador usa o fluxo de vídeo HTML5 no formato HLS. E ele se baseia na reprodução progressiva do HTML5 em determinados sistemas, como o Internet Explorer e o Android™ mais antigos. </p> <p>Quando <span class="codeph"> progressive</span> é definido, o visualizador depende apenas da reprodução de HTML5 como suportado de forma nativa pelos navegadores e reproduz vídeo progressivamente em todos os sistemas. </p> <p>Para obter mais informações sobre a seleção de reprodução nos modos nativos <span class="codeph"> auto</span> e <span class="codeph"> progressive</span>, consulte o Guia do Usuário do HTML5 Viewers SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional. Ignorado quando o visualizador funciona com vídeo externo.

Consulte [Suporte de vídeo externo](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) para obter detalhes.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`auto`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive`
