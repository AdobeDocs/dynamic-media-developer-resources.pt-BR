---
description: Atributo de configuração para o visualizador do Video360.
seo-description: Atributo de configuração para o visualizador do Video360.
seo-title: Video360Player.posterimage
solution: Experience Manager
title: Video360Player.posterimage
uuid: a1adc3b7-2ea3-4f26-84f2-b5c2f4418038
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo 360 VR
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 7%

---


# Video360Player.posterimage{#video-player-posterimage}

Atributo de configuração para o visualizador do Video360.

` [Video360Player.|<containerId>_video360Player.]posterimage=none|[? *`isCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nenhum|[?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> Modificadores do Image Serving que controlam a aparência da imagem de pôster. Se especificado no URL, codifique o seguinte por HTTP: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> como  <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> como  <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> como  <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p> Esse modificador funciona para o conteúdo de vídeo hospedado no Dynamic Media Classic ou AEM Dynamic Media. </p> <p>Para evitar a exibição da imagem de pôster padrão, especifique <span class="codeph"> none</span> como o valor da imagem de pôster. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

Nenhum.

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
posterimage=none
```

