---
description: Entrega de vídeo HTTPS
solution: Experience Manager
title: Entrega de vídeo HTTPS
uuid: 7f8c1fe6-b464-4d80-9ffe-a36081825d49
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídias mistas
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---


# Entrega de vídeo HTTPS{#https-video-delivery}

>[!NOTE]
>
>A entrega de vídeo seguro se aplica somente ao AEM 6.2 com a instalação do [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) e ao AEM 6.1 com a instalação do [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

Desde que o visualizador funcione na configuração conforme descrito no início desta seção, a entrega de vídeo publicado pode ocorrer nos modos HTTPS (seguro) e HTTP (inseguro). Em uma configuração padrão, o protocolo de entrega de vídeo segue estritamente o protocolo de entrega da página da Web de incorporação. No entanto, é possível forçar a entrega de vídeo HTTPS independentemente do protocolo usado ao incorporar a página da Web usando o atributo de configuração [VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e). (Observe que a visualização de vídeo no modo Autor é sempre fornecida com segurança por HTTPS.)

Dependendo do método de publicação de vídeo do Dynamic Media usado no AEM, o atributo de configuração `VideoPlayer.ssl` é aplicado de forma diferente, conforme demonstrado no seguinte:

* Se você publicar um vídeo do Dynamic Media com um URL, anexe `VideoPlayer.ssl` ao URL. Por exemplo, para forçar a entrega segura de vídeo, você anexa `&VideoPlayer.ssl=on` ao final do seguinte exemplo de URL do visualizador:

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/MixedMediaViewer.html?asset=%2Fcontent%2Fdam%2FGeometrixx-Outdoors-New-Launch%2Fbackpack%2Fbackpack_mixed_media&config=/etc/dam/presets/viewer/MixedMedia_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&VideoPlayer.ssl=on
   ```

   Consulte também [(Vincular URLs ao seu Aplicativo Web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic).

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

   Consulte também [(Incorporando o vídeo em uma página da Web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic).

