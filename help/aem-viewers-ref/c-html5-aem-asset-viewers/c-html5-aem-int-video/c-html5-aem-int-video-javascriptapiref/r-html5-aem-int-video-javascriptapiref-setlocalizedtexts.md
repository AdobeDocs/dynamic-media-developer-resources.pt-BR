---
description: Referência da API JavaScript para o Visualizador de vídeo interativo.
seo-description: Referência da API JavaScript para o Visualizador de vídeo interativo.
seo-title: setLocalizedTexts
solution: Experience Manager
title: setLocalizedTexts
topic: Dynamic media
uuid: 11844a71-adb0-42a9-9b58-b69821070fd2
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# setLocalizedTexts{#setlocalizedtexts}

Referência da API JavaScript para o Visualizador de vídeo interativo.

` setLocalizedTexts( *`localizationInfo`*)`

Define os valores SYMBOL de localização para uma ou mais localidades. Esse parâmetro deve ser chamado antes `init()`.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo </span></span> </p> </td> 
   <td colname="col2"> <p> Objeto { <span class="codeph"> Object </span>} JSON com dados de localização. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Localização de elementos da interface do usuário </a> para obter mais informações. </p> <p>Consulte também o Guia <i>do usuário do SDK do</i> visualizador e o exemplo para obter mais informações sobre o conteúdo do objeto. </p> </td> 
  </tr> 
 </tbody> 
</table>

Consulte também [init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played."},"fr":{"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus."},defaultLocale:"en"})
```

