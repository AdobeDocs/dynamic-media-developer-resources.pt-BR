---
title: setLocalizedTexts
description: setLocalizedTexts
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 313069b6-f114-487a-8322-55b4dff43f68
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 0%

---

# setLocalizedTexts{#setlocalizedtexts}

` setLocalizedTexts( *`informaçõesDeLocalização`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo </span> </span> </p> </td> 
   <td colname="col2"> <p> Objeto JSON <span class="codeph"> do </span> objeto com dados de localização. </p> <p>Consulte o namespace <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-namespace.md#concept-679bfabb3e3e4c12a285c4e9c4144153" format="dita" scope="local"> do SDK do visualizador </a> para obter mais informações. </p> <p>Consulte o <i>Guia do Usuário do Visualizador do SDK</i> e o exemplo para obter mais informações sobre o conteúdo do objeto. Opcional. </p> </td> 
  </tr> 
 </tbody> 
</table>

Define valores de SYMBOL de localização para um ou mais locais. Este parâmetro deve ser chamado antes de `init()`.

Consulte também [init](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"SmartCropVideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played."},"fr":{"SmartCropVideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus."},defaultLocale:"en"})
```
