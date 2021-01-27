---
description: Suporte para rastreamento do Adobe Analytics
solution: Experience Manager
title: Suporte para rastreamento do Adobe Analytics
topic: Dynamic Media
uuid: 0d4dee7b-3ffb-4bf5-93b1-67972bfc9b2a
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# Suporte para rastreamento do Adobe Analytics{#support-for-adobe-analytics-tracking}

Por padrão, o visualizador envia uma solicitação HTTP de rastreamento único para o Servidor de imagens configurado com as informações de tipo e versão do visualizador.

## Acompanhamento personalizado {#section-cda48fc9730142d0bb3326bac7df3271}

Para integrar sistemas de análise de terceiros, é necessário ouvir o `trackEvent` retorno de chamada do visualizador e processar o argumento `eventInfo` da função de retorno de chamada, conforme necessário. O código a seguir é um exemplo dessa função de manipulador:

```
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
}, 
"handlers":{ 
 "trackEvent":function(objID, compClass, instName, timeStamp, eventInfo) { 
  //identify event type 
  var eventType = eventInfo.split(",")[0]; 
  switch (eventType) { 
   case "LOAD": 
    //custom event processing code 
    break; 
   case "INTERACTIVE_SWATCH": 
    //custom event processing code which handles user clicks on interactive swatches 
    break; 
   //additional cases for other events 
} 
} 
} 
});
```

O visualizador rastreia os seguintes eventos de usuário do SDK:

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Evento de usuário do SDK </p> </th> 
   <th colname="col2" class="entry"> <p>Enviado... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CARREGAR  </span> </p> </td> 
   <td colname="col2"> <p>quando o visualizador é carregado primeiro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP  </span> </p> </td> 
   <td colname="col2"> <p>quando um ativo é trocado no visualizador usando a API <span class="codeph"> setAsset() </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> JOGAR  </span> </p> </td> 
   <td colname="col2"> <p>quando a reprodução for start. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSA  </span> </p> </td> 
   <td colname="col2"> <p>quando a reprodução é pausada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PARAR  </span> </p> </td> 
   <td colname="col2"> <p>quando a reprodução for interrompida. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MARCO  </span> </p> </td> 
   <td colname="col2"> <p>quando a reprodução atinge um dos seguintes marcos: 0%, 25%, 50%, 75% ou 100%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> INTERATIVE_SWATCH  </span> </p> </td> 
   <td colname="col2"> <p>sempre que o usuário clicar em uma amostra interativa. </p> </td> 
  </tr> 
 </tbody> 
</table>

