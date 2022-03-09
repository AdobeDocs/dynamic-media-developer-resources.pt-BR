---
title: Suporte para rastreamento do Adobe Analytics
description: O Visualizador de rotação é compatível com o rastreamento Adobe Analytics pronto para uso.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User,Data Engineer,Data Architect
exl-id: 30762700-6d69-4299-9492-57893232abe1
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---

# Suporte para rastreamento do Adobe Analytics{#support-for-adobe-analytics-tracking}

O Visualizador de rotação é compatível com o rastreamento Adobe Analytics pronto para uso.

## Rastreamento pronto para uso {#section-d06145cfa2b9491bb485b599368d466e}

O Visualizador de rotação é compatível com o rastreamento de Adobe Analytics pronto para uso.

Para ativar o rastreamento, passe o nome predefinido da empresa apropriado como `config2` parâmetro.

O visualizador também envia uma única solicitação HTTP de rastreamento para o Servidor de imagens configurado com o tipo de visualizador e as informações da versão.

## Rastreamento personalizado {#section-47512156a1d64b338b50cfa39c84f4aa}

Para integrar com sistemas de análise de terceiros, é necessário ouvir o `trackEvent` retorno de chamada do visualizador e processe o `eventInfo` argumento da função de retorno de chamada, conforme necessário. O código a seguir é um exemplo dessa função de manipulador:

```javascript {.line-numbers}
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
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
   <th colname="col2" class="entry"> <p>Enviado quando... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CARREGAR </span> </p> </td> 
   <td colname="col2"> <p>O visualizador é carregado primeiro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>um ativo é trocado no visualizador usando o <span class="codeph"> setAsset() </span> API. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p> uma imagem é ampliada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN </span> </p> </td> 
   <td colname="col2"> <p>uma imagem é ativada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SPIN </span> </p> </td> 
   <td colname="col2"> <p> um spin é executado. </p> </td> 
  </tr> 
 </tbody> 
</table>
