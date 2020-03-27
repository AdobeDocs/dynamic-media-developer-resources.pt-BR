---
description: Referência da API JavaScript para Visualizador de zoom básico.
seo-description: Referência da API JavaScript para Visualizador de zoom básico.
seo-title: BasicZoomViewer
solution: Experience Manager
title: BasicZoomViewer
topic: Dynamic media
uuid: 727e38af-636a-4eb3-b373-6940169d006b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# BasicZoomViewer{#basiczoomviewer}

Referência da API JavaScript para Visualizador de zoom básico.

`BasicZoomViewer([config])`

Construtor, cria uma nova instância do Visualizador de zoom básico.

## Parâmetros {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configuração </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> O objeto de configuração JSON opcional {object} </span> permite que todas as configurações do visualizador passem para o construtor para evitar chamar métodos de setter individuais. Contém as seguintes propriedades: </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID do container DOM (normalmente um <span class="codeph"> DIV </span>) no qual o visualizador é inserido. Quando esse método é chamado, não é necessário ter o elemento de container criado. No entanto, o container deve existir quando <span class="codeph"> init() </span> é executado. Obrigatório. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params </span> - objeto JSON <span class="codeph"> {Object} </span> com parâmetros de configuração do visualizador, onde o nome da propriedade é a opção de configuração específica do visualizador ou o modificador SDK, e o valor dessa propriedade é um valor de configurações correspondente. Obrigatório. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> manipuladores </span> - <span class="codeph"> {Object} </span> objeto JSON com retornos de chamada de evento do visualizador, onde o nome da propriedade é o nome do evento do visualizador suportado e o valor da propriedade é uma referência de função JavaScript para retorno de chamada apropriado. Opcional. </p> <p>Consulte Retornos de chamada do <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-event-callbacks.md#concept-8ba57cf86537401999514e1b221ec734" format="dita" scope="local"> Evento </a> para obter mais informações sobre eventos do visualizador. </p> </li> 
      <li id="li_528FE03845F847E08F964E38D6AB6E86"> <p> <span class="codeph"> localizedTexts </span> - objeto <span class="codeph"> {Object} </span> JSON com dados de localização. Opcional. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Localização de elementos da interface do usuário </a> para obter mais informações. </p> <p> Consulte também o Guia <i>do usuário do SDK do</i> visualizador e o exemplo para obter mais informações sobre o conteúdo do objeto. Opcional </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
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

