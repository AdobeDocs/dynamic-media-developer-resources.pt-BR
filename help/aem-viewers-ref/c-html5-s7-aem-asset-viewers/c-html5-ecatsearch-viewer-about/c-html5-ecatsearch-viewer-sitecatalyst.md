---
description: O eCatalog Search Viewer oferece suporte para o rastreamento Adobe Analytics fora da caixa.
seo-description: O eCatalog Search Viewer oferece suporte para o rastreamento Adobe Analytics fora da caixa.
seo-title: Suporte para rastreamento do Adobe Analytics
solution: Experience Manager
title: Suporte para rastreamento do Adobe Analytics
topic: Dynamic Media
uuid: 2e1e2bc6-5372-4ba2-b6d7-8b760b1b0a8a
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---


# Suporte para rastreamento do Adobe Analytics{#support-for-adobe-analytics-tracking}

O eCatalog Search Viewer oferece suporte para o rastreamento Adobe Analytics fora da caixa.

## Rastreamento predefinido {#section-ba994f079d0343c8ae48adffaa3195a3}

O eCatalog Search Viewer suporta [!DNL Adobe Analytics] rastreamento predefinido. Para ativar o rastreamento, passe o nome predefinido de empresa como parâmetro `config2`.

O visualizador também envia uma solicitação HTTP de rastreamento único para o Servidor de imagens configurado com as informações de tipo e versão do visualizador.

## Acompanhamento personalizado {#section-cda48fc9730142d0bb3326bac7df3271}

Para integrar sistemas de análise de terceiros, é necessário ouvir o `trackEvent` retorno de chamada do visualizador e processar o argumento `eventInfo` da função de retorno de chamada, conforme necessário. O código a seguir é um exemplo dessa função de manipulador:

```
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
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
   <td colname="col1"> <p> <span class="codeph"> CARREGAR  </span> </p> </td> 
   <td colname="col2"> <p>o visualizador é carregado primeiro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP  </span> </p> </td> 
   <td colname="col2"> <p>um ativo é trocado no visualizador usando a API <span class="codeph"> setAsset() </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM  </span> </p> </td> 
   <td colname="col2"> <p> uma imagem é ampliada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN  </span> </p> </td> 
   <td colname="col2"> <p>uma imagem está em um plano. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWATCH  </span> </p> </td> 
   <td colname="col2"> <p> uma imagem é alterada ao clicar ou tocar em uma amostra. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PÁGINA  </span> </p> </td> 
   <td colname="col2"> <p> um quadro atual é alterado na visualização principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ITEM  </span> </p> </td> 
   <td colname="col2"> <p>um pop-up do painel de informações é ativado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF  </span> </p> </td> 
   <td colname="col2"> <p>um usuário navega para uma página diferente devido ao clique no mapa de imagem. </p> </td> 
  </tr> 
 </tbody> 
</table>

