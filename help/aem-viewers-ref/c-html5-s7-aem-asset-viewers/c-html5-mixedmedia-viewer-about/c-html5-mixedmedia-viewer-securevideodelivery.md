---
title: Entrega de vídeo HTTPS
description: Entrega de vídeo HTTPS
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: f9651405-ebc6-4b1f-8fb6-031d0b295083
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# Entrega de vídeo HTTPS{#https-video-delivery}

<!-- >[!NOTE]
>
>Secure Video Delivery only applies to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

Se o visualizador funcionar na configuração conforme descrito no início desta seção, a entrega de vídeo publicado poderá ocorrer nos modos HTTPS (seguro) e HTTP (inseguro). Em uma configuração padrão, o protocolo de entrega de vídeo segue rigorosamente o protocolo de entrega da página da Web de incorporação. No entanto, é possível forçar a entrega de vídeos HTTPS independentemente do protocolo usado ao incorporar a página da Web usando o atributo de configuração [VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e). (A visualização de vídeo no modo Autor é sempre fornecida com segurança por HTTPS.)

Dependendo do método de publicação de vídeos do Dynamic Media usado no Adobe Experience Manager, o atributo de configuração `VideoPlayer.ssl` é aplicado de forma diferente, conforme demonstrado a seguir:

* Se você publicar um vídeo do Dynamic Media com uma URL, anexe `VideoPlayer.ssl` à URL. Por exemplo, para forçar a entrega de vídeo segura, você anexa `&VideoPlayer.ssl=on` ao final do seguinte exemplo de URL do visualizador:

  ```
  https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/MixedMediaViewer.html?asset=%2Fcontent%2Fdam%2FGeometrixx-Outdoors-New-Launch%2Fbackpack%2Fbackpack_mixed_media&config=/etc/dam/presets/viewer/MixedMedia_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&VideoPlayer.ssl=on
  ```

  Consulte também [(Vincular URLs ao Aplicativo Web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic).

* Se você publicar um vídeo do Dynamic Media com código incorporado, adicione `VideoPlayer.ssl` à lista de outros parâmetros de configuração do visualizador no trecho de código incorporado. Por exemplo, para forçar a entrega de vídeo HTTPS, você anexa `&VideoPlayer.ssl=on` como no exemplo a seguir:

  ```
  <style type="text/css"> 
   #s7mixedmedia_div.s7mixedmediaviewer{ 
     width:100%;  
     height:auto; 
   } 
  </style> 
  <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/MixedMediaViewer.js"></script> 
  <div id="s7mixedmedia_div"></div> 
  <script type="text/javascript"> 
   var s7mixedmediaviewer = new s7viewers.MixedMediaViewer({ 
    "containerId" : "s7mixedmedia_div", 
    "params" : {  
     "VideoPlayer.ssl" : "on", 
     "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
     "contenturl" : "https://demos-pub.assetsadobe.com/",  
     "config" : "/etc/dam/presets/viewer/MixedMedia_light", 
     "config2": "/etc/dam/presets/analytics", 
     "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
     "asset" : "/content/dam/Geometrixx-Outdoors-New-Launch/backpack/backpack_mixed_media" } 
   }).init(); 
  </script>
  ```

  Consulte também [(Incorporação do Vídeo em uma Página da Web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic).
