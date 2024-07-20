---
title: VideoViewer
description: Referência da API do JavaScript para o Visualizador de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 4ba152e6-b5a9-4e81-b9f8-aa987a1c31f9
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# VideoViewer{#videoviewer}

Referência da API do JavaScript para o Visualizador de vídeo.

`VideoViewer([config])`

Construtor; cria uma nova instância do Visualizador de vídeo.

## Parâmetros {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> objeto de configuração JSON opcional, permite que todas as configurações do visualizador sejam passadas para o construtor e evite chamar métodos setter individuais. Contém as seguintes propriedades: </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID do contêiner DOM (normalmente um <span class="codeph"> DIV </span>) no qual o visualizador está inserido. Não é necessário criar o elemento de contêiner quando esse método for chamado. No entanto, o contêiner deve existir quando <span class="codeph"> init() </span> é executado. Obrigatório. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> parâmetros </span> - <span class="codeph"> {Object} </span> objeto JSON com parâmetros de configuração de visualizador em que o nome da propriedade é uma opção de configuração específica do visualizador ou um modificador SDK, e o valor dessa propriedade é um valor de configurações correspondente. Obrigatório. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> manipuladores </span> - <span class="codeph"> {Object} </span> objeto JSON com retornos de chamada de evento do visualizador, em que o nome da propriedade é o nome do evento do visualizador com suporte, e o valor da propriedade é uma referência de função JavaScript para um retorno de chamada apropriado. Opcional. <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-event-callbacks.md#concept-ebe5a4c1853d4912a919d86df35c1f6d" format="dita" scope="local"> retornos de chamada de evento </a> para obter mais informações sobre eventos do visualizador. </p> </li> 
      <li id="li_D344288C9B584E569F7BF92D960F9DF8"> <p> <span class="codeph"> localizedTexts </span> - { <span class="codeph"> Objeto </span>} objeto JSON com dados de localização. Opcional. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-namespace.md#concept-679bfabb3e3e4c12a285c4e9c4144153" format="dita" scope="local"> Namespace do SDK do visualizador </a> para obter mais informações. </p> <p>Consulte o <i>Guia do Usuário do Visualizador do SDK</i> e o exemplo para obter mais informações sobre o conteúdo do objeto. Opcional. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played." 
}, 
"fr":{ 
"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus." 
}, 
defaultLocale:"en" 
} 
});
```
