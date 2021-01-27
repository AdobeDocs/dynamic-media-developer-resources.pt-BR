---
description: Suporte para rastreamento de análises
solution: Experience Manager
title: Suporte para rastreamento de análises
topic: Dynamic Media
uuid: ae870d2e-2a09-4551-935a-916d0e657653
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---


# Suporte para rastreamento de análises{#support-for-analytics-tracking}

## Acompanhamento personalizado {#section-cda48fc9730142d0bb3326bac7df3271}

Por padrão, o visualizador envia uma única solicitação HTTP de rastreamento para o Servidor de imagens configurado com o tipo de visualizador e as informações de versão.

Para integrar sistemas de análise de terceiros, é necessário ouvir o `trackEvent` retorno de chamada do visualizador e processar o argumento `eventInfo` da função de retorno de chamada, conforme necessário. O código a seguir é um exemplo dessa função de manipulador:

```
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
  "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
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
   <td colname="col1"> <p> <span class="codeph"> HREF  </span> </p> </td> 
   <td colname="col2"> <p>o usuário ativa o hotspot. </p> </td> 
  </tr> 
 </tbody> 
</table>

