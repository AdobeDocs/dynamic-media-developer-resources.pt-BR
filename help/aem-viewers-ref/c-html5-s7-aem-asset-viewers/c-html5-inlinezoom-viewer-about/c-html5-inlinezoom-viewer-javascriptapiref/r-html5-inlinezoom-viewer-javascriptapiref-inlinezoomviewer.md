---
description: Referência da API do JavaScript para o Visualizador de Zoom em Linha.
seo-description: Referência da API do JavaScript para o Visualizador de Zoom em Linha.
seo-title: FlyoutViewer
solution: Experience Manager
title: FlyoutViewer
uuid: 23617eda-f4c9-4908-9f63-593849c12fc7
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom em linha
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---


# FlyoutViewer{#flyoutviewer}

Referência da API do JavaScript para o Visualizador de Zoom em Linha.

`FlyoutViewer([config])`

Construtor; cria uma nova instância do Visualizador de Zoom em Linha.

## Parâmetros {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configuração  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} objeto de configuração JSON  </span> opcional, permite que todas as configurações do visualizador passem para o construtor e evitem chamar métodos de setter individuais. Contém as seguintes propriedades: </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}  </span> ID do contêiner DOM (normalmente um  <span class="codeph"> DIV  </span>) no qual o visualizador é inserido. Não é necessário ter o elemento container criado pelo momento em que esse método é chamado. No entanto, o contêiner deve existir quando <span class="codeph"> init() </span> é executado. Obrigatório. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> params  </span> -  <span class="codeph"> {Object} objeto  </span> JSON com parâmetros de configuração do visualizador, onde o nome da propriedade é uma opção de configuração específica do visualizador ou um modificador de SDK, e o valor dessa propriedade é um valor de configurações correspondente. Obrigatório. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> manipuladores  </span> - objeto  <span class="codeph"> {Object}  </span> JSON com retornos de chamada do evento do visualizador, onde o nome da propriedade é o nome do evento do visualizador suportado, e o valor da propriedade é uma referência de função JavaScript para um retorno de chamada apropriado. Opcional. <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-event-callbacks.md#concept-53eb01d28189437790268da4929f2a10" format="dita" scope="local"> Retornos de chamada do evento </a> para obter mais informações sobre os eventos do visualizador. </p> </li> 
      <li id="li_218F9597A60249AEBA43A9E86EAFF8BA"> <p> <span class="codeph"> localizedTexts  </span> - {  <span class="codeph"> Object  </span>} objeto JSON com dados de localização. Opcional. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local"> Localização dos elementos da interface do usuário </a> para obter mais informações. </p> <p>Consulte o <i>Guia do usuário do SDK do visualizador</i> e o exemplo para obter mais informações sobre o conteúdo do objeto. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom" 
}, 
"fr":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer" 
}, 
defaultLocale:"en" 
} 
});
```

