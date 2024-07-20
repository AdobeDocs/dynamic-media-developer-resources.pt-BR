---
title: Entrega de vídeo HTTP
description: Entrega de vídeo HTTP
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 33907e22-107b-4345-82bb-cad47cb7a839
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# Entrega de vídeo HTTP{#http-video-delivery}

<!-- >[!NOTE]
>
>Secure Video Delivery only applies to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

Se o visualizador funcionar na configuração conforme descrito no início desta seção, a entrega de vídeo publicado poderá ocorrer nos modos HTTPS (seguro) e HTTP (inseguro). Em uma configuração padrão, o protocolo de entrega de vídeo segue rigorosamente o protocolo de entrega da página da Web de incorporação. No entanto, é possível forçar a entrega de vídeos HTTPS independentemente do protocolo usado ao incorporar a página da Web usando o atributo de configuração [VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e). (A visualização de vídeo no modo Autor é sempre fornecida com segurança por HTTPS.)

Dependendo do método de publicação de vídeos do Dynamic Media usado no Adobe Experience Manager, o atributo de configuração `VideoPlayer.ssl` é aplicado de forma diferente, conforme demonstrado a seguir:

* Se você publicar um vídeo do Dynamic Media com uma URL, anexe `VideoPlayer.ssl` à URL. Por exemplo, para forçar a entrega de vídeo segura, você anexa `&VideoPlayer.ssl=on` ao final do seguinte exemplo de URL do visualizador:

  ```
  https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/VideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&VideoPlayer.ssl=on
  ```

  Consulte também [Vincular URLs ao Aplicativo Web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic).

* Se você publicar um vídeo do Dynamic Media com código incorporado, adicione `VideoPlayer.ssl` à lista de outros parâmetros de configuração do visualizador no trecho de código incorporado. Por exemplo, para forçar a entrega de vídeo HTTPS, você anexa `&VideoPlayer.ssl=on` como no exemplo a seguir:

  ```
  <style type="text/css"> 
   #s7video_div.s7videoviewer{ 
     width:100%;  
     height:auto; 
   } 
  </style> 
  <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/VideoViewer.js"></script> 
  <div id="s7video_div"></div> 
  <script type="text/javascript"> 
   var s7videoviewer = new s7viewers.VideoViewer({ 
    "containerId" : "s7video_div", 
    "params" : {  
     "VideoPlayer.ssl" : "on", 
     "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
     "contenturl" : "https://demos-pub.assetsadobe.com/",  
     "config" : "/etc/dam/presets/viewer/Video", 
     "config2": "/etc/dam/presets/analytics", 
     "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
     "posterimage": "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4", 
     "asset" : "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4" } 
   }).init(); 
  </script>
  ```

  Consulte também [Incorporação do vídeo em uma página da Web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic).
