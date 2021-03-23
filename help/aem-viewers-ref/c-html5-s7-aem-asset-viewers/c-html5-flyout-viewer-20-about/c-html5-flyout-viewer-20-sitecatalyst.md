---
description: O Flyout Viewer é compatível com o rastreamento Adobe Analytics pronto para uso.
seo-description: O Flyout Viewer é compatível com o rastreamento Adobe Analytics pronto para uso.
seo-title: Suporte para rastreamento do Adobe Analytics
solution: Experience Manager
title: Suporte para rastreamento do Adobe Analytics
uuid: 204857d3-744a-4c11-90db-1b18ff5ea5df
feature: Dynamic Media Classic,Visualizadores,SDK/API,Flyout
role: Desenvolvedor,Profissional de negócios,Engenheiro de dados,Arquiteto de dados
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# Suporte para rastreamento do Adobe Analytics{#support-for-adobe-analytics-tracking}

O Flyout Viewer é compatível com o rastreamento Adobe Analytics pronto para uso.

## Rastreamento pronto para uso {#section-ba994f079d0343c8ae48adffaa3195a3}

O Flyout Viewer suporta [!DNL Adobe Analytics] rastreamento pronto para uso. Para ativar o rastreamento, passe o nome predefinido da empresa apropriado como parâmetro `config2`.

O visualizador também envia uma única solicitação HTTP de rastreamento para o Servidor de imagens configurado com o tipo de visualizador e as informações da versão.

## Rastreamento personalizado {#section-cda48fc9730142d0bb3326bac7df3271}

Para integrar com sistemas de análise de terceiros, é necessário ouvir o retorno de chamada do visualizador `trackEvent` e processar o argumento `eventInfo` da função de retorno de chamada conforme necessário. O código a seguir é um exemplo dessa função de manipulador:

```
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
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
   <td colname="col2"> <p>o flyout é ativado ou o nível de zoom é alterado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN  </span> </p> </td> 
   <td colname="col2"> <p> uma imagem é ativada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWATCH  </span> </p> </td> 
   <td colname="col2"> <p> uma imagem é alterada ao clicar ou tocar em uma amostra. </p> </td> 
  </tr> 
 </tbody> 
</table>

