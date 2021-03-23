---
description: Referência da API do JavaScript para o visualizador do Video360.
seo-description: Referência da API do JavaScript para o visualizador do Video360.
seo-title: getComponent
solution: Experience Manager
title: getComponent
uuid: 2f10c080-f21d-4021-b10c-cd83f731db65
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo 360 VR
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---


# getComponent{#getcomponent}

Referência da API do JavaScript para o visualizador do Video360.

`getComponent(componentId)`

Retorna uma referência ao componente do SDK do visualizador usado pelo visualizador. A página da Web pode usar esse método para estender ou personalizar o comportamento do visualizador pronto para uso. Chame esse método somente depois que o retorno de chamada do visualizador `initComplete` for executado, caso contrário, o componente ainda não poderá ser criado pela lógica do visualizador.

## Parâmetros {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*`  -  `{String}` uma ID do componente do SDK do visualizador usado pelo visualizador. Esse visualizador é compatível com as seguintes IDs de componente:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ID do componente </p> </th> 
   <th colname="col2" class="entry"> <p>Nome da classe do componente SDK do visualizador </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> container  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> video360Player  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.Video360Player  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fullScreenButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.FullScreenButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mutableVolume  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.MutableVolume  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> playPauseButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PlayPauseButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoScrubber  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.VideoScrubber  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoTime  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.VideoTime  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> controles  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ControlBar  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> socialShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.SocialShare  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> twitterShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.TwitterShare  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> facebookShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.FacebookShare  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> linkShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.LinkShare  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> embedShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sk.share.EmbedShare  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Ao trabalhar com APIs do SDK, é importante usar o namespace do SDK totalmente qualificado conforme descrito em [Namespace do SDK do visualizador](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-viewer-sdk-namespace.md#concept-4ee8657c7d67421f8e7880130a246621).

Consulte a documentação do *HTML5 Viewer SDK API* para obter mais informações sobre um componente específico.

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` uma referência ao componente do SDK do visualizador. O método retornará `null` se `componentId` não for um componente do visualizador suportado ou se o componente ainda não tiver sido criado pela lógica do visualizador.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var video360Player = <instance>.getComponent("video360Player"); 
} 
})
```

