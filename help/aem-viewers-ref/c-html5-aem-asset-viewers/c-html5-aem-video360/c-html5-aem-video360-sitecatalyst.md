---
title: Suporte para rastreamento do Adobe Analytics
description: Suporte para rastreamento do Adobe Analytics
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User,Data Engineer,Data Architect
exl-id: fb58a388-e4da-475d-b726-d5a32e99cce0
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Suporte para rastreamento do Adobe Analytics{#support-for-adobe-analytics-tracking}

Por padrão, o visualizador envia uma única solicitação HTTP de rastreamento ao Servidor de imagens configurado com o tipo de visualizador e informações de versão.

## Rastreamento personalizado {#section-cda48fc9730142d0bb3326bac7df3271}

Para integrar com sistemas de análise de terceiros, é necessário ouvir o retorno de chamada do visualizador `trackEvent` e processar o argumento `eventInfo` da função de retorno de chamada conforme necessário. O código a seguir é um exemplo dessa função de manipulador:

```javascript {.line-numbers}
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
   <td colname="col1"> <p> <span class="codeph"> CARREGAR </span> </p> </td> 
   <td colname="col2"> <p>quando o visualizador é carregado primeiro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TROCA </span> </p> </td> 
   <td colname="col2"> <p>quando um ativo é trocado no visualizador usando a API <span class="codeph"> do </span> setAsset(). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> JOGAR </span> </p> </td> 
   <td colname="col2"> <p>quando a reprodução começa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSAR </span> </p> </td> 
   <td colname="col2"> <p>quando a reprodução é pausada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PARADA </span> </p> </td> 
   <td colname="col2"> <p>quando a reprodução é interrompida. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ETAPA </span> </p> </td> 
   <td colname="col2"> <p>quando a reprodução atingir um dos seguintes marcos: 0%, 25%, 50%, 75% ou 100%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AMOSTRA_INTERATIVA </span> </p> </td> 
   <td colname="col2"> <p>sempre que o usuário clicar em uma amostra interativa. </p> </td> 
  </tr> 
 </tbody> 
</table>
