---
title: Suporte para rastreamento do Adobe Analytics
description: Suporte para rastreamento do Adobe Analytics
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User,Data Engineer,Data Architect
exl-id: fb58a388-e4da-475d-b726-d5a32e99cce0
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# Suporte para rastreamento do Adobe Analytics{#support-for-adobe-analytics-tracking}

Por padrão, o visualizador envia uma única solicitação HTTP de rastreamento a um Servidor de imagens configurado com informações de tipo de visualizador e versão.

## Rastreamento personalizado {#section-cda48fc9730142d0bb3326bac7df3271}

Para integrar a sistemas analíticos de terceiros, é necessário acompanhar `trackEvent` retorno de chamada e processo do visualizador `eventInfo` argumento da função de retorno de chamada, conforme necessário. O código a seguir é um exemplo dessa função de manipulador:

```javascript {.line-numbers}
var panoramicViewer = new s7viewers.PanoramicViewer({
    "containerId":"s7viewer",
"params":{
    "asset":"Scene7SharedAssets/PanoramicImage-Sample",
    "serverurl":"http://s7d1.scene7.com/is/image/"
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
   <th colname="col2" class="entry"> <p>Enviado... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CARREGAR </span> </p> </td> 
   <td colname="col2"> <p>quando o visualizador é carregado primeiro. </p> </td> 
  </tr> 
 </tbody> 
</table>
