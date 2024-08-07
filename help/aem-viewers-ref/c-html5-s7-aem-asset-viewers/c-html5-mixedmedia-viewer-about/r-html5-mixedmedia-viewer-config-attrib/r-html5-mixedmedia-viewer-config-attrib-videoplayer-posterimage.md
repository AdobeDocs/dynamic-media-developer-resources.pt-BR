---
title: VideoPlayer.posterimage
description: VideoPlayer.posterimage
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: bcbba4c5-b758-4049-b4c2-f1c48cc2de7e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# VideoPlayer.posterimage{#videoplayer-posterimage}

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommands`*]`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nenhum|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> A imagem a ser exibida no primeiro quadro antes do início da reprodução do vídeo, resolvida em relação a <span class="codeph"> serverurl</span>. Se especificado no URL, HTTP-encode o seguinte: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph">?</span> como <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> as <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> como <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Se o valor de <span class="codeph"><span class="varname"> image_id</span></span> for omitido, o componente tentará usar a imagem de pôster padrão para esse ativo. </p> <p>Quando o vídeo é especificado como um caminho, a ID de catálogo de imagens de pôster padrão é derivada do caminho do vídeo como o par <span class="codeph"> catalog_id/image_id</span>, onde <span class="codeph"> catalog_id</span> corresponde ao primeiro token no caminho. E <span class="codeph"> image_id</span> é o nome do vídeo com a extensão removida. Se a imagem com essa ID não existir, a imagem do pôster não será exibida. </p> <p>Para impedir a exibição da imagem de pôster padrão, especifique <span class="codeph"> none</span> como o valor da imagem de pôster. Se apenas <span class="codeph"><span class="varname"> isCommands</span></span> forem especificados, os comandos serão aplicados à imagem de pôster padrão antes que a imagem seja exibida. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

Nenhum.

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`posterimage=none`
