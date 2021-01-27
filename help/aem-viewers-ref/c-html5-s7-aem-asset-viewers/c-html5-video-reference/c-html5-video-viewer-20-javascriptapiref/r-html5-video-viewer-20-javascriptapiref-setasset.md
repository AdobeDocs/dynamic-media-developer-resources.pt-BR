---
description: Referência da API JavaScript para o Visualizador de vídeo.
seo-description: Referência da API JavaScript para o Visualizador de vídeo.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic Media
uuid: 7543126c-5cc3-4010-ad7f-8d2e8d643133
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---


# setAsset{#setasset}

Referência da API JavaScript para o Visualizador de vídeo.

`setAsset(asset[, data])`

Define o novo ativo e os dados opcionais do ativo adicional. Você pode chamar esse parâmetro a qualquer momento, antes ou depois de `init()`. Se for chamado depois de `init()`, o visualizador alternará o ativo em tempo de execução.

Consulte também [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## Parâmetros {#section-e030b401b966469cb5dd121501161c2a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ativo  </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>} nova ID de ativo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> data  </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> JSON </span>} objeto JSON com os seguintes campos opcionais (diferencia maiúsculas de minúsculas): </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> posterimage  </span> - Imagem a ser exibida no primeiro quadro antes da reprodução dos start de vídeo. Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-cmdref/r-html5-video-viewer-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage </a>. </li> 
      <li id="li_BBFF3965B69A4AC8A469FDB69097B25A"> <span class="codeph"> caption  </span> - local do novo arquivo de legenda. Se o arquivo não for especificado, o botão de legenda fechada não estará visível na interface do usuário. </li> 
      <li id="li_4659E82D38EB4438AAA04FDEAF21B087"> <span class="codeph"> navigation  </span> - URL ou caminho para o conteúdo de navegação WebVTT. O arquivo WebVTT deve ser servido pelo Serviço de Imagens </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Scene7SharedAssets/Glacier_Climber_MP4")
```

