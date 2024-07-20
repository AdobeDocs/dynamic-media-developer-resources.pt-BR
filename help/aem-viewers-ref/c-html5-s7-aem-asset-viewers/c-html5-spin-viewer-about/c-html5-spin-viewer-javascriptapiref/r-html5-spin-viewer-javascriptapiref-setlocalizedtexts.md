---
title: setLocalizedTexts
description: Referência da API do JavaScript para o Visualizador de rotação.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 840c7e13-8998-4479-b0fc-f96a615a0a58
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 0%

---

# setLocalizedTexts{#setlocalizedtexts}

Referência da API do JavaScript para o Visualizador de rotação.

` setLocalizedTexts( *`informaçõesDeLocalização`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> Objeto {<span class="codeph">} objeto JSON </span> com dados de localização. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98" format="dita" scope="local"> Localização dos elementos da interface do usuário</a> para obter mais informações. </p> <p>Consulte também o <i>Guia do Usuário do Visualizador do SDK</i> e o exemplo para obter mais informações sobre o conteúdo do objeto. </p> </td> 
  </tr> 
 </tbody> 
</table>

Define valores de SYMBOL de localização para um ou mais locais. Este parâmetro deve ser chamado antes de `init()`.

Consulte também [init](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```
