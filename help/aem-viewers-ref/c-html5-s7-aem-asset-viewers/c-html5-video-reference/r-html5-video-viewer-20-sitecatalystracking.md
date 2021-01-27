---
description: O Visualizador de vídeo oferece suporte ao rastreamento Adobe Analytics pronto para uso.
seo-description: O Visualizador de vídeo oferece suporte ao rastreamento Adobe Analytics pronto para uso.
seo-title: Suporte para rastreamento do Adobe Analytics
solution: Experience Manager
title: Suporte para rastreamento do Adobe Analytics
topic: Dynamic Media
uuid: c53b3d3b-42e5-4c87-8a1e-87c73eb32341
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---


# Suporte para rastreamento do Adobe Analytics{#support-for-adobe-analytics-tracking}

O Visualizador de vídeo oferece suporte ao rastreamento Adobe Analytics pronto para uso.

## Rastreamento predefinido {#section-3b101fe30be943c1b679fd5c273569ca}

O Visualizador de vídeo oferece suporte ao rastreamento Adobe Analytics pronto para uso.

Para ativar o rastreamento, passe o nome predefinido de empresa como parâmetro `config2`.

O visualizador também envia uma solicitação HTTP de rastreamento único para o Servidor de imagens configurado com as informações de tipo e versão do visualizador.

## Acompanhamento personalizado {#section-ab10bd7caf184721a366cf3953071934}

Para integrar com sistemas de análise de terceiros, é necessário ouvir `trackEvent` o retorno de chamada do visualizador e processar `eventInfo` o argumento da função de retorno de chamada, conforme necessário. O código a seguir é um exemplo dessa função de manipulador:

```
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
}, 
"handlers":{ 
 "trackEvent":function(objID, compClass, instName, timeStamp, eventInfo) { 
  //identify event type 
  var eventType = eventInfo.split(",")[0]; 
  switch (eventType) { 
   case "LOAD": 
    //custom event processing code 
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
   <th colname="col2" class="entry"> <p>Enviado quando... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CARREGAR  </span> </p> </td> 
   <td colname="col2"> <p>o visualizador é carregado primeiro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP  </span> </p> </td> 
   <td colname="col2"> <p>um ativo é trocado no visualizador usando a API <span class="codeph"> setAsset() </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> JOGAR  </span> </p> </td> 
   <td colname="col2"> <p>a reprodução é iniciada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSA  </span> </p> </td> 
   <td colname="col2"> <p>a reprodução está pausada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PARAR  </span> </p> </td> 
   <td colname="col2"> <p>a reprodução é interrompida. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MARCO  </span> </p> </td> 
   <td colname="col2"> <p>a reprodução atinge um dos seguintes marcos: 0%, 25%, 50%, 75% e 100%. </p> </td> 
  </tr> 
 </tbody> 
</table>

