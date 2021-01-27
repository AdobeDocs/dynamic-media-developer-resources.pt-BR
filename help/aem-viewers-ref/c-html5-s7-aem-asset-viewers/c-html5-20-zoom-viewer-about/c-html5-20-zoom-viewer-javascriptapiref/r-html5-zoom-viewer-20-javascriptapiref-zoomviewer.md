---
description: Referência da API JavaScript para Visualizador de zoom.
seo-description: Referência da API JavaScript para Visualizador de zoom.
seo-title: ZoomViewer
solution: Experience Manager
title: ZoomViewer
topic: Dynamic Media
uuid: 4c2acfaf-cc42-4bb7-a830-7226a8007117
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# ZoomViewer{#zoomviewer}

Referência da API JavaScript para Visualizador de zoom.

`ZoomViewer([config])`

Construtor, cria uma nova instância do Visualizador de zoom.

## Parâmetros {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configuração  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> O objeto de configuração JSON  </span> opcional {object} permite que todas as configurações do visualizador passem para o construtor para evitar chamar métodos setter individuais. Contém as seguintes propriedades: </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}  </span> ID do container DOM (normalmente um  <span class="codeph"> DIV  </span>) no qual o visualizador é inserido. Quando esse método é chamado, não é necessário ter o elemento de container criado. No entanto, o container deve existir quando <span class="codeph"> init() </span> for executado. Obrigatório. </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <span class="codeph"> params  </span> - objeto  <span class="codeph"> {Object}  </span> JSON com parâmetros de configuração do visualizador em que o nome da propriedade é a opção de configuração específica do visualizador ou o modificador SDK, e o valor dessa propriedade é um valor de configurações correspondente. Obrigatório. </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <span class="codeph"> manipuladores  </span> - objeto  <span class="codeph"> {Object}  </span> JSON com retornos de chamada de evento do visualizador, onde o nome da propriedade é o nome do evento do visualizador suportado e o valor da propriedade é uma referência de função JavaScript para retorno de chamada apropriado. Opcional. <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> retornos de chamada do Evento </a> para obter mais informações sobre eventos do visualizador. </p> </li> 
      <li id="li_1D181A6B1D434B29B09AFD3F4BE059BD"> <span class="codeph"> localizedTexts  </span> - objeto  <span class="codeph"> {Object}  </span> JSON com dados de localização. Opcional. <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Localização de elementos da interface do usuário </a> para obter mais informações. </p> <p>Consulte também <i>Guia do usuário do Viewer SDK</i> e o exemplo para obter mais informações sobre o conteúdo do objeto. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"CloseButton.TOOLTIP":"Close" 
}, 
"fr":{ 
"CloseButton.TOOLTIP":"Fermer" 
}, 
defaultLocale:"en" 
} 
});
```

