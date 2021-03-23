---
description: Referência da API JavaScript para visualizador de vídeo
seo-description: Referência da API JavaScript para visualizador de vídeo
seo-title: setVideo
solution: Experience Manager
title: setVideo
uuid: 0a1b3caa-ded6-4020-962c-41c3ece0a865
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---


# setVideo{#setvideo}

Referência da API JavaScript para visualizador de vídeo

`setVideo(videoUrl[, data])`

Define o novo vídeo externo e os dados de vídeo adicionais opcionais. Pode ser chamado a qualquer momento, antes e depois de `init()`. Se chamado depois de `init()`, o visualizador troca o vídeo em tempo de execução.

Consulte também [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## Parâmetros {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl  </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> Cadeia de caracteres </span>} é um URL absoluto para o novo vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dados  </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> JSON </span>} objeto JSON com os seguintes campos opcionais (diferencia maiúsculas de minúsculas): </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> posterimage  </span> - Imagem a ser exibida no primeiro quadro antes da reprodução do vídeo. Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-cmdref/r-html5-video-viewer-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage </a>. </li> 
      <li id="li_4659E82D38EB4438AAA04FDEAF21B087"> <span class="codeph"> caption  </span> - Localização do novo arquivo de legenda. Se nenhum arquivo de legenda for especificado, o botão de legenda não será exibido na interface do usuário. </li> 
      <li id="li_A43A1BAB6B0F4A7981F71408F08F07D1"> <span class="codeph"> navegação  </span> - URL ou caminho para o conteúdo de navegação da WebVTT. O arquivo WebVTT deve ser distribuído pelo Serviço de Imagens. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setVideo("https://s7d9.scene7.com/is/content/Scene7SharedAssets/Glacier_Climber_MP4")
```

