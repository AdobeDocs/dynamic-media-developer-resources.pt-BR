---
description: O eCatalog Search Viewer oferece suporte ao rastreamento Adobe Analytics pronto para uso.
solution: Experience Manager
title: Suporte para rastreamento do Adobe Analytics
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User,Data Engineer,Data Architect
exl-id: b35e52f5-fa08-4945-aa52-9fdf41a6081a
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# Suporte para rastreamento do Adobe Analytics{#support-for-adobe-analytics-tracking}

O eCatalog Search Viewer oferece suporte ao rastreamento Adobe Analytics pronto para uso.

## Rastreamento pronto para uso {#section-ba994f079d0343c8ae48adffaa3195a3}

O Visualizador de Pesquisa do Catálogo Eletrônico é compatível [!DNL Adobe Analytics] rastreamento pronto para uso. Para ativar o rastreamento, passe o nome predefinido da empresa apropriado como `config2` parâmetro.

O visualizador também envia uma única solicitação HTTP de rastreamento para o Servidor de imagens configurado com o tipo de visualizador e as informações da versão.

## Rastreamento personalizado {#section-cda48fc9730142d0bb3326bac7df3271}

Para integrar-se a sistemas de análise de terceiros, é necessário ouvir o `trackEvent` retorno de chamada do visualizador e processe o `eventInfo` argumento da função de retorno de chamada, conforme necessário. O código a seguir é um exemplo dessa função de manipulador:

```javascript {.line-numbers}
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/" 
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
   <td colname="col1"> <p> <span class="codeph"> SWATCH </span> </p> </td> 
   <td colname="col2"> <p> uma imagem é alterada ao clicar ou tocar em uma amostra. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PÁGINA </span> </p> </td> 
   <td colname="col2"> <p> um quadro atual é alterado na exibição principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ITEM </span> </p> </td> 
   <td colname="col2"> <p>um pop-up do painel de informações é ativado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>um usuário navega para uma página diferente devido ao clique do mapa de imagem. </p> </td> 
  </tr> 
 </tbody> 
</table>
