---
title: SpinViewer
description: Referência da API do JavaScript para o Visualizador de rotação.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 0cfde665-c578-41a0-a428-0db3cbdac6ae
TQID: 'https://experienceleague.adobe.com/-aZhpoZiLqC8B77Ajt8wPTLBC3Z7zwcTiF9bPjndglg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 205
ht-degree: 0%

---

# SpinViewer{#spinviewer}

Referência da API do JavaScript para o Visualizador de rotação.

`SpinViewer([config])`

Construtor, cria uma nova instância do visualizador de rotação.

## Parâmetros {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> objeto de configuração JSON opcional, permite que todas as configurações do visualizador sejam passadas para o construtor e evite chamar métodos setter individuais. Contém as seguintes propriedades: </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID do contêiner DOM (normalmente um <span class="codeph"> DIV </span>) no qual o visualizador está inserido. Não é necessário criar o elemento de contêiner quando esse método for chamado. No entanto, o contêiner deve existir quando <span class="codeph"> init() </span> é executado. Obrigatório. </p> </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <p> <span class="codeph"> parâmetros </span> - <span class="codeph"> {Object} </span> objeto JSON com parâmetros de configuração de visualizador em que o nome da propriedade é uma opção de configuração específica do visualizador ou um modificador SDK, e o valor dessa propriedade é um valor de configurações correspondente. Obrigatório. </p> </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <p> <span class="codeph"> manipuladores </span> - <span class="codeph"> {Object} </span> objeto JSON com retornos de chamada de evento do visualizador, em que o nome da propriedade é o nome do evento do visualizador com suporte, e o valor da propriedade é uma referência de função JavaScript para um retorno de chamada apropriado. Opcional. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-event-callbacks.md#concept-9c553c80eefd422faacf6522c69804bf" format="dita" scope="local"> retornos de chamada de evento </a> para obter mais informações sobre eventos do visualizador. </p> </li> 
      <li id="li_643787FB4A424D0AB6B8E12F44C3A9AC"> <p> <span class="codeph"> objeto JSON localizadoTexts </span> - <span class="codeph"> {Object} </span> com dados de localização. Opcional. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98" format="dita" scope="local"> Localização dos elementos da interface do usuário </a> para obter mais informações. </p> <p>Consulte também o <i>Guia do Usuário do Visualizador do SDK</i> e o exemplo para obter mais informações sobre o conteúdo do objeto. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
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
