---
description: VideoPlayer.posterimage
solution: Experience Manager
title: VideoPlayer.posterimage
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídias mistas
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---


# VideoPlayer.posterimage{#videoplayer-posterimage}

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_`*][? *`idisCommands`*]`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nenhum|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> A imagem a ser exibida no primeiro quadro antes que o vídeo comece a ser reproduzido, resolvida em <span class="codeph"> serverurl</span>. Se especificado no URL, codifique o seguinte por HTTP: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> como  <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> como  <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> como  <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Se o valor <span class="codeph"><span class="varname"> image_id</span></span> for omitido, o componente tentará usar a imagem de pôster padrão para esse ativo. </p> <p>Quando o vídeo é especificado como um caminho, a id de catálogo de imagens de pôster padrão é derivada do caminho do vídeo como o par <span class="codeph"> catalog_id/image_id</span> onde <span class="codeph"> catalog_id</span> corresponde ao primeiro token no caminho e <span class="codeph"> image_id</span> é o nome do vídeo com a extensão removida. Se a imagem com essa ID não existir, a imagem de pôster não será exibida. </p> <p>Para evitar a exibição da imagem de pôster padrão, especifique <span class="codeph"> none</span> como o valor da imagem de pôster. Se apenas <span class="codeph"><span class="varname"> isCommands</span></span> forem especificados, os comandos serão aplicados à imagem de pôster padrão antes que a imagem seja exibida. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

Nenhum.

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`posterimage=none`
