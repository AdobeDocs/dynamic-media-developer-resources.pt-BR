---
description: Atributo de configuração para o Visualizador de vídeo.
seo-description: Atributo de configuração para o Visualizador de vídeo.
seo-title: VideoPlayer.posterimage
solution: Experience Manager
title: VideoPlayer.posterimage
topic: Dynamic Media
uuid: 59d81a72-ac17-4c32-ab47-89bd14dc17a5
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---


# VideoPlayer.posterimage{#videoplayer-posterimage}

Atributo de configuração para o Visualizador de vídeo.

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_`*][? *`idisCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> A imagem a ser exibida no primeiro quadro antes da reprodução dos start de vídeo foi resolvida em <span class="codeph"> serverurl</span>. Se especificado no URL, codifique o seguinte por HTTP: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> como  <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> como  <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> como  <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Se o valor <span class="codeph"><span class="varname"> image_id</span></span> for omitido, o componente tentará usar a imagem de pôster padrão para esse ativo. </p> <p>Quando o vídeo é especificado como um caminho, a ID de catálogo de imagens de pôster padrão é derivada do caminho do vídeo como o par <span class="codeph"> Catalog_id/image_id</span> no qual <span class="codeph"> Catalog_id</span> corresponde ao primeiro token no caminho e <span class="codeph"> image_id</span> é o nome do vídeo com a extensão removida. Se a imagem com essa ID não existir, a imagem do pôster não será exibida. </p> <p>Para impedir a exibição da imagem de pôster padrão, especifique <span class="codeph"> none</span> como o valor da imagem de pôster. Se apenas <span class="codeph"><span class="varname"> isCommands</span></span> forem especificados, os comandos serão aplicados à imagem de pôster padrão antes que a imagem seja exibida. </p> </td> 
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

