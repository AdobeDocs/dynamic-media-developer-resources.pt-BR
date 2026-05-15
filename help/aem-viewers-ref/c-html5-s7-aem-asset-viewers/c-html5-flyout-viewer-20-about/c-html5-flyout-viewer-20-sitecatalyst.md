---
title: Suporte para rastreamento do Adobe Analytics
description: O Visualizador de imagem suspensa é compatível com o rastreamento de Adobe Analytics pronto para uso.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 6b6216f4-34dc-496f-a0c3-e97d48da14c6
TQID: 'https://experienceleague.adobe.com/UFgX6X7iRmQ8T0iZgdqmnidxEWsTq8mAJv7PDFBlUwA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 174
ht-degree: 0%

---

# Suporte para rastreamento do Adobe Analytics{#support-for-adobe-analytics-tracking}

O Visualizador de imagem suspensa é compatível com o rastreamento de Adobe Analytics pronto para uso.

## Rastreamento pronto para uso {#section-ba994f079d0343c8ae48adffaa3195a3}

O Visualizador de Submenu oferece suporte para [!DNL Adobe Analytics] rastreamento pronto para uso. Para habilitar o rastreamento, passe o nome de predefinição da empresa correto como o parâmetro `config2`.

O visualizador também envia uma única solicitação HTTP de rastreamento ao Servidor de imagens configurado com o tipo de visualizador e informações de versão.

## Rastreamento personalizado {#section-cda48fc9730142d0bb3326bac7df3271}

Para integrar com sistemas de análise de terceiros, é necessário ouvir o retorno de chamada do visualizador `trackEvent` e processar o argumento `eventInfo` da função de retorno de chamada conforme necessário. O código a seguir é um exemplo dessa função de manipulador:

```javascript {.line-numbers}
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
   <td colname="col1"> <p> <span class="codeph"> CARREGAR </span> </p> </td> 
   <td colname="col2"> <p>o visualizador é carregado primeiro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TROCA </span> </p> </td> 
   <td colname="col2"> <p>um ativo é trocado no visualizador usando a API </span> do <span class="codeph"> setAsset(). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p>a imagem suspensa está ativada ou o nível de zoom foi alterado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PANORÂMICA </span> </p> </td> 
   <td colname="col2"> <p> uma imagem é exibida em modo panorâmico. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AMOSTRA </span> </p> </td> 
   <td colname="col2"> <p> uma imagem é alterada ao clicar ou tocar em uma amostra. </p> </td> 
  </tr> 
 </tbody> 
</table>
