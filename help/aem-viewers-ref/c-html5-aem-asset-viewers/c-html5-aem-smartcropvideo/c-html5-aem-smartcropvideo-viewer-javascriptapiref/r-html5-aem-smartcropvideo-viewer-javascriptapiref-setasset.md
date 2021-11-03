---
title: setAsset
description: Referência da API do JavaScript para o visualizador de vídeo de recorte inteligente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: e5d71393-fcae-4bd4-8e78-a451b2f05ffc
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---

# setAsset{#setasset}

Referência da API do JavaScript para o visualizador de vídeo de recorte inteligente.

`setAsset(asset[, data])`

Define o novo ativo e os dados opcionais do ativo adicional. Você pode chamar esse parâmetro a qualquer momento, antes ou depois de `init()`. Se for chamado depois de `init()`, o visualizador troca o ativo no tempo de execução.

Consulte também [init]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref\r-html5-aem-smartcropvideo-viewer-javascript-tapiref-init.md#md referência-3b570ba8b35045d6b30fb178c21a66c6).

## Parâmetros {#section-e030b401b966469cb5dd121501161c2a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ativo </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>} nova ID de ativo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dados </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> JSON </span>} Objeto JSON com os seguintes campos opcionais (diferencia maiúsculas de minúsculas): </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> posterimage </span> - Imagem a ser exibida no primeiro quadro antes da reprodução do vídeo. Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-cmdref/r-html5-aem-smartcropvideo-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage </a>. </li> 
      <li id="li_BBFF3965B69A4AC8A469FDB69097B25A"> <span class="codeph"> caption </span> - local do novo arquivo de legenda fechada. Se o arquivo não for especificado, o botão de legenda não estará visível na interface do usuário. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Scene7SharedAssets/Glacier_Climber_MP4")
```
