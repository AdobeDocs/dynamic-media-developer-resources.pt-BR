---
title: SmartCropVideoPlayer.ssl
description: Atributo de configuração para o Visualizador de Corte inteligente de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 590ef156-0afe-4e65-b84b-b33f7c7d7b02
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# SmartCropVideoPlayer.ssl{#smartcropvideoplayer-ssl}

Atributo de configuração para o Visualizador de Corte inteligente de vídeo.

<!-- >[!NOTE]
>
>This configuration attribute only applies to AEM 6.2 with installation of [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

`[SmartCropVideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|em</span> </p> </td> 
   <td colname="col2"> <p> Controla se o vídeo é entregue por uma conexão SSL segura (HTTPS) ou por uma conexão insegura (HTTP). </p> <p>Quando definido como <span class="codeph"> auto</span>, o protocolo de entrega de vídeo é herdado do protocolo da página da Web incorporada. Se a página da Web for carregada por HTTPS, o vídeo também será entregue por HTTPS e vice-versa. Se a página da Web estiver em HTTP, o vídeo será entregue via HTTP. </p> <p>Quando definido como <span class="codeph"> em</span>, a entrega de vídeo sempre ocorre através de uma conexão segura, independentemente do protocolo da página da Web. </p> <p>Afeta somente a entrega de vídeo publicado e é ignorado para visualização de vídeo no modo Autor. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
ssl=on
```

<!--<a id="section_5943AC73316749C68761FF7F74DA7547"></a>-->

Consulte também [Entrega de vídeo segura](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-securevideodelivery.md#concept-cf9d1346a07d4429b0c6c32c9cac50ff).
