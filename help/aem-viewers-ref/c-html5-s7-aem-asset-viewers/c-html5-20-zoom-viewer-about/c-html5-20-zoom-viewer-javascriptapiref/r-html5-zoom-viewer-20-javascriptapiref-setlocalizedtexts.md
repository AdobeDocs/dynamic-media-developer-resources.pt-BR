---
description: Referência da API do JavaScript para o Visualizador de vídeo.
seo-description: Referência da API do JavaScript para o Visualizador de vídeo.
seo-title: setLocalizedTexts
solution: Experience Manager
title: setLocalizedTexts
uuid: af1844bb-1af2-4efb-9824-2371ec91b342
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---


# setLocalizedTexts{#setlocalizedtexts}

Referência da API do JavaScript para o Visualizador de vídeo.

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> Objeto</span>} objeto JSON com dados de localização. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Localização dos elementos da interface do usuário</a> para obter mais informações. </p> <p>Consulte também <i>Guia do usuário do SDK do visualizador</i> e o exemplo para obter mais informações sobre o conteúdo do objeto. </p> </td> 
  </tr> 
 </tbody> 
</table>

Define valores SYMBOL de localização para uma ou mais localidades. Esse parâmetro deve ser chamado antes de `init()`.

Consulte também [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```

