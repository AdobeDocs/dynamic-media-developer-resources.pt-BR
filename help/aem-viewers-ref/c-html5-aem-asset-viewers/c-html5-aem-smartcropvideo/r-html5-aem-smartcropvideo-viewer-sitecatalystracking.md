---
title: Suporte para rastreamento do Adobe Analytics
description: O Visualizador de vídeo de recorte inteligente é compatível com o rastreamento de Adobe Analytics pronto para uso.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 0d91ca94-79fc-40de-8095-0252688ebe76
TQID: 'https://experienceleague.adobe.com/qxJCNOQ6B6iYDi7JRepZfc9gMaF4Wn50DoPYWnTsq5Y'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 177
ht-degree: 0%

---

# Suporte para rastreamento do Adobe Analytics{#support-for-adobe-analytics-tracking}

O Visualizador de vídeo de recorte inteligente é compatível com o rastreamento de Adobe Analytics pronto para uso.

## Rastreamento pronto para uso {#section-3b101fe30be943c1b679fd5c273569ca}

O Visualizador de vídeo de recorte inteligente é compatível com o rastreamento de Adobe Analytics pronto para uso.

Para habilitar o rastreamento, passe o nome de predefinição da empresa correto como o parâmetro `config2`.

O visualizador também envia uma única solicitação HTTP de rastreamento ao Servidor de imagens configurado com o tipo de visualizador e informações de versão.

## Rastreamento personalizado {#section-ab10bd7caf184721a366cf3953071934}

Para integrar com sistemas de análise de terceiros, é necessário ouvir o retorno de chamada do visualizador `trackEvent` e processar o argumento `eventInfo` da função de retorno de chamada conforme necessário. O código a seguir é um exemplo dessa função de manipulador:

```javascript {.line-numbers}
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
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
   <td colname="col1"> <p> <span class="codeph"> CARREGAR </span> </p> </td> 
   <td colname="col2"> <p>o visualizador é carregado primeiro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TROCA </span> </p> </td> 
   <td colname="col2"> <p>um ativo é trocado no visualizador usando a API </span> do <span class="codeph"> setAsset(). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> JOGAR </span> </p> </td> 
   <td colname="col2"> <p>reprodução iniciada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSAR </span> </p> </td> 
   <td colname="col2"> <p>reprodução em pausa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PARADA </span> </p> </td> 
   <td colname="col2"> <p>reprodução interrompida. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ETAPA </span> </p> </td> 
   <td colname="col2"> <p>a reprodução atinge uma das seguintes millstones: 0%, 25%, 50%, 75% e 100%. </p> </td> 
  </tr> 
 </tbody> 
</table>
