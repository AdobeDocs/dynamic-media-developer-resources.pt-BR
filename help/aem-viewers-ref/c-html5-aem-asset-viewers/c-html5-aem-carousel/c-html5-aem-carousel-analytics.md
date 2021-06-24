---
description: Suporte para rastreamento do Adobe Analytics
solution: Experience Manager
title: Suporte para rastreamento do Adobe Analytics
feature: Dynamic Media Classic,Visualizadores,SDK/API,Banners em carrossel
role: Developer,Business Practitioner,Data Engineer,Data Architect
exl-id: 9e321684-4861-4d81-b55c-66c77635930e
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---

# Suporte para rastreamento do Adobe Analytics{#support-for-adobe-analytics-tracking}

## Rastreamento personalizado {#section-cda48fc9730142d0bb3326bac7df3271}

Por padrão, o visualizador envia uma única solicitação de rastreamento HTTP para o Image Server configurado com o tipo de visualizador e as informações da versão.

Para integrar com sistemas de análise de terceiros, é necessário ouvir o retorno de chamada do visualizador `trackEvent` e processar o argumento `eventInfo` da função de retorno de chamada conforme necessário. O código a seguir é um exemplo dessa função de manipulador:

```
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
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
   <td colname="col1"> <p> <span class="codeph"> BANNER  </span> </p> </td> 
   <td colname="col2"> <p>a imagem do banner do carrossel é alterada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF  </span> </p> </td> 
   <td colname="col2"> <p>o usuário ativa o ponto de acesso. </p> </td> 
  </tr> 
 </tbody> 
</table>
