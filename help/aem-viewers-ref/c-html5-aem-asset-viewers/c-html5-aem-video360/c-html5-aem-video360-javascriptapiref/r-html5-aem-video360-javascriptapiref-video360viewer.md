---
description: Referência da API do JavaScript para o visualizador do Video360.
solution: Experience Manager
title: Visualizador de vídeo360
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo 360 VR
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---


# Visualizador de vídeo360a{#video-viewer}

Referência da API do JavaScript para o visualizador do Video360.

`Video360Viewer([config])`

Construtor, cria uma nova instância do Visualizador de vídeo HTML5 360.

## Parâmetros {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configuração  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} objeto de configuração JSON  </span> opcional, permite que todas as configurações do visualizador sejam enviadas ao construtor para evitar chamar métodos de setter individuais. Contém as seguintes propriedades: </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}  </span> ID do contêiner DOM (normalmente um  <span class="codeph"> DIV  </span>) no qual o visualizador é inserido. Quando esse método é chamado, não é necessário criar o elemento container. No entanto, o contêiner deve existir quando <span class="codeph"> init() </span> é executado. </p> <p>Obrigatório. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params  </span> - objeto  <span class="codeph"> {Object}  </span> JSON com parâmetros de configuração do visualizador em que o nome da propriedade é a opção de configuração específica do visualizador ou o modificador SDK, e o valor dessa propriedade é um valor de configurações correspondente. </p> <p>Obrigatório. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> manipuladores  </span> - objeto  <span class="codeph"> {Object}  </span> JSON com retornos de chamada do evento do visualizador, onde o nome da propriedade é o nome do evento do visualizador suportado e o valor da propriedade é uma referência de função JavaScript para o retorno de chamada apropriado. </p> <p>Opcional. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Retornos de chamada do evento </a> para obter mais informações sobre os eventos do visualizador. </p> </li> 
      <li id="li_42A3F3BEF1004E069F0FB2AE0A30B093"> <p> <span class="codeph"> localizedTexts  </span> - objeto  <span class="codeph"> {Object}  </span> JSON com dados de localização. Opcional. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local"> Localização dos elementos da interface do usuário </a> para obter mais informações. </p> <p>Consulte também o <i>Guia do usuário do SDK do visualizador</i> e o exemplo para obter mais informações sobre o conteúdo do objeto. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"Video360Player.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played." 
}, 
"fr":{ 
"Video360Player.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus." 
}, 
defaultLocale:"en" 
} 
});
```

