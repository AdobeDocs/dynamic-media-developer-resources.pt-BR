---
title: CarouselViewer
description: Referência da API do JavaScript para o Visualizador do carrossel.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 890d869d-dbf2-4c24-88d1-34c439ab1e3a
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 1%

---

# CarouselViewer{#carouselviewer}

Referência da API do JavaScript para o Visualizador do carrossel.

`CarouselViewer([config])`

Construtor, cria uma instância HTML 5 do Visualizador de carrossel.

## Parâmetros {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configuração </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> objeto de configuração JSON opcional, permite que todas as configurações do visualizador sejam transmitidas ao construtor para evitar chamar métodos de setter individuais. Contém as seguintes propriedades: </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID do contêiner DOM (normalmente um <span class="codeph"> DIV </span>) em que o visualizador é inserido. Quando esse método é chamado, não é necessário criar o elemento container. No entanto, o contêiner deve existir quando <span class="codeph"> init() </span> é executado. </p> <p>Obrigatório. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params </span> - <span class="codeph"> {Objeto} </span> Objeto JSON com parâmetros de configuração do visualizador em que o nome da propriedade é a opção de configuração específica do visualizador ou o modificador de SDK, e o valor dessa propriedade é um valor de configurações correspondente. </p> <p>Obrigatório. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> manipuladores </span> - <span class="codeph"> {Objeto} </span> Objeto JSON com retornos de chamada do evento do visualizador, em que o nome da propriedade é o nome do evento do visualizador suportado e o valor da propriedade é uma referência de função JavaScript para o retorno de chamada apropriado. </p> <p>Opcional. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Retornos de chamada do evento </a> para obter mais informações sobre eventos do visualizador. </p> </li> 
      <li id="li_CD88EDB586B241DBB87B13709F24C454"> <p> <span class="codeph"> localizedTexts </span> - <span class="codeph"> {Objeto} </span> </p> <p> Objeto JSON com dados de localização. Consulte Localização dos elementos da interface do usuário e o exemplo para obter mais informações sobre o conteúdo do objeto. </p> <p>Opcional </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"PanLeftButton.TOOLTIP":"Left" 
}, 
"fr":{ 
"PanLeftButton.TOOLTIP":"Gauchiste" 
}, 
defaultLocale:"en" 
} 
});
```
