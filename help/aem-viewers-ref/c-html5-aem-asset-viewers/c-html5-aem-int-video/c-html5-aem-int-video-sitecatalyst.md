---
description: O HTML5 Video360 Viewer oferece suporte ao Adobe Analytics para rastreamento imediato.
seo-description: O HTML5 Video360 Viewer oferece suporte ao Adobe Analytics para rastreamento imediato.
seo-title: Suporte para rastreamento do Adobe Analytics
solution: Experience Manager
title: Suporte para rastreamento do Adobe Analytics
topic: Dynamic media
uuid: b5ab903b-3365-45e3-9542-c290c6c42670
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Suporte para rastreamento do Adobe Analytics{#support-for-adobe-analytics-tracking}

O HTML5 Video360 Viewer oferece suporte ao Adobe Analytics para rastreamento imediato.

Para ativar o rastreamento, passe o nome predefinido de empresa como `config2` parâmetro.

Por padrão, o visualizador envia uma solicitação HTTP de rastreamento único para o Servidor de imagens configurado com as informações de tipo e versão do visualizador.

## Acompanhamento personalizado {#section-cda48fc9730142d0bb3326bac7df3271}

Para integrar sistemas de análise de terceiros, é necessário ouvir o retorno de chamada do `trackEvent` visualizador e processar o `eventInfo` argumento da função de retorno de chamada, conforme necessário. O código a seguir é um exemplo dessa função de manipulador:

```
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
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
   <th colname="col1" class="entry"> <p>evento de usuário do SDK </p> </th> 
   <th colname="col2" class="entry"> <p>Enviado... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CARREGAR </span> </p> </td> 
   <td colname="col2"> <p>quando o visualizador é carregado primeiro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>quando um ativo é trocado no visualizador usando <span class="codeph"> setAsset() </span> API. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> JOGAR </span> </p> </td> 
   <td colname="col2"> <p>quando a reprodução for start. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSA </span> </p> </td> 
   <td colname="col2"> <p>quando a reprodução é pausada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PARAR </span> </p> </td> 
   <td colname="col2"> <p>quando a reprodução for interrompida. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MARCO </span> </p> </td> 
   <td colname="col2"> <p>quando a reprodução atinge um dos seguintes marcos: 0%, 25%, 50%, 75% ou 100%. </p> </td> 
  </tr> 
 </tbody> 
</table>

