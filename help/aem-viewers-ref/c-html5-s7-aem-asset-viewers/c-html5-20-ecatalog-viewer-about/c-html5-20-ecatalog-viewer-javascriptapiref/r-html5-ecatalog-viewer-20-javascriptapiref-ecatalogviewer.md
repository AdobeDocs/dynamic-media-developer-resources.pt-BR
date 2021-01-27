---
description: Referência da API JavaScript para o eCatalog Viewer.
seo-description: Referência da API JavaScript para o eCatalog Viewer.
seo-title: eCatalogViewer
solution: Experience Manager
title: eCatalogViewer
topic: Dynamic Media
uuid: b87b6f6b-3e83-47b3-b867-30eca5eae56b
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---


# eCatalogViewer{#ecatalogviewer}

Referência da API JavaScript para o eCatalog Viewer.

`eCatalogViewer([config])`

Construtor, cria uma nova instância do eCatalog Viewer.

## Parâmetros {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configuração  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> O objeto de configuração JSON  </span> opcional {Object} permite que todas as configurações do visualizador passem para o construtor e evitem chamar métodos setter individuais. Contém as seguintes propriedades: </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <p> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}  </span> ID do container DOM (normalmente um  <span class="codeph"> DIV  </span>) no qual o visualizador é inserido. Não é necessário ter o elemento de container criado no momento em que esse método é chamado. No entanto, o container deve existir quando <span class="codeph"> init() </span> for executado. Obrigatório. </p> </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <p> <span class="codeph"> params  </span> - objeto  <span class="codeph"> {Object}  </span> JSON com parâmetros de configuração do visualizador, onde o nome da propriedade é uma opção de configuração específica do visualizador ou um modificador SDK, e o valor dessa propriedade é um valor de configurações correspondente. Obrigatório. </p> </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <p> <span class="codeph"> manipuladores  </span> - objeto  <span class="codeph"> {Object}  </span> JSON com retornos de chamada de evento do visualizador, onde o nome da propriedade é o nome do evento do visualizador suportado, e o valor da propriedade é uma referência de função JavaScript para um retorno de chamada apropriado. Opcional. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-event-callbacks.md#concept-0bf5ff877043468db58ac62a92d002b6" format="dita" scope="local"> retornos de chamada do Evento </a> para obter mais informações sobre eventos do visualizador. </p> </li> 
      <li id="li_FE5B330E98834CB08C16FCA694F31BE3"> <p> <span class="codeph"> localizedTexts  </span> - objeto JSON {  <span class="codeph"> Object  </span>} com dados de localização. Opcional. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Localização de elementos da interface do usuário </a> para obter mais informações. </p> <p>Consulte também o <i>Guia do usuário do Viewer SDK</i> e o exemplo para obter mais informações sobre o conteúdo do objeto. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
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

