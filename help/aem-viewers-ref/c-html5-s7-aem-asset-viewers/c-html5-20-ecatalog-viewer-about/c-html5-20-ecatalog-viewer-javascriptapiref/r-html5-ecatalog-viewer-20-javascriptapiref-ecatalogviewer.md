---
title: eCatalogViewer
description: Referência da API do JavaScript para o Visualizador do eCatalog.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 111699a3-8a70-4caf-b7da-7b594b785f7c
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# eCatalogViewer{#ecatalogviewer}

Referência da API do JavaScript para o Visualizador do eCatalog.

`eCatalogViewer([config])`

Construtor, cria uma instância do Visualizador de eCatalog.

## Parâmetros {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configuração </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Objeto} </span> objeto de configuração JSON opcional, permite que todas as configurações do visualizador sejam passadas para o construtor e evite chamar métodos de setter individuais. Contém as seguintes propriedades: </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID do contêiner DOM (normalmente um <span class="codeph"> DIV </span>) em que o visualizador é inserido. Não é necessário ter o elemento container criado pelo momento em que esse método é chamado. No entanto, o contêiner deve existir quando <span class="codeph"> init() </span> é executado. Obrigatório. </p> </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <p> <span class="codeph"> params </span> - <span class="codeph"> {Objeto} </span> Objeto JSON com parâmetros de configuração do visualizador, onde o nome da propriedade é uma opção de configuração específica do visualizador ou um modificador de SDK, e o valor dessa propriedade é um valor de configurações correspondente. Obrigatório. </p> </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <p> <span class="codeph"> manipuladores </span> - <span class="codeph"> {Objeto} </span> Objeto JSON com retornos de chamada do evento do visualizador, em que o nome da propriedade é o nome do evento do visualizador suportado e o valor da propriedade é uma referência de função JavaScript para um retorno de chamada apropriado. Opcional. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-event-callbacks.md#concept-0bf5ff877043468db58ac62a92d002b6" format="dita" scope="local"> Retornos de chamada do evento </a> para obter mais informações sobre eventos do visualizador. </p> </li> 
      <li id="li_FE5B330E98834CB08C16FCA694F31BE3"> <p> <span class="codeph"> localizedTexts </span> - { <span class="codeph"> Objeto </span>} Objeto JSON com dados de localização. Opcional. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Localização dos elementos da interface do usuário </a> para obter mais informações. </p> <p>Consulte também a <i>Guia do usuário do SDK do visualizador</i> e o exemplo para obter mais informações sobre o conteúdo do objeto. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/" 
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
