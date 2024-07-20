---
title: setLocalizedTexts
description: Referência da API do JavaScript para o Visualizador de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 89d6231d-8063-435f-864e-c352287e4764
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 0%

---

# setLocalizedTexts{#setlocalizedtexts}

Referência da API do JavaScript para o Visualizador de vídeo.

` setLocalizedTexts( *`informaçõesDeLocalização`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> Objeto {<span class="codeph">} objeto JSON </span> com dados de localização. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Localização dos elementos da interface do usuário</a> para obter mais informações. </p> <p>Consulte também o <i>Guia do Usuário do Visualizador do SDK</i> e o exemplo para obter mais informações sobre o conteúdo do objeto. </p> </td> 
  </tr> 
 </tbody> 
</table>

Define valores de SYMBOL de localização para um ou mais locais. Este parâmetro deve ser chamado antes de `init()`.

Consulte também [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```
