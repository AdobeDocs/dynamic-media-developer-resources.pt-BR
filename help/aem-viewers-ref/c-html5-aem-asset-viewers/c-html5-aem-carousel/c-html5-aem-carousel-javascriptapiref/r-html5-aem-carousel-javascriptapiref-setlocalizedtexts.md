---
description: Referência da API do JavaScript para o Visualizador do carrossel.
seo-description: Referência da API do JavaScript para o Visualizador do carrossel.
seo-title: setLocalizedTexts
solution: Experience Manager
title: setLocalizedTexts
uuid: f69d3232-dd7c-41b5-87a0-146b8fb1bdb1
feature: Dynamic Media Classic,Visualizadores,SDK/API,Banners em carrossel
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---


# setLocalizedTexts{#setlocalizedtexts}

Referência da API do JavaScript para o Visualizador do carrossel.

` setLocalizedTexts( *`localizationInfo`*)`

Define valores SYMBOL de localização para uma ou mais localidades. Esse parâmetro deve ser chamado antes de `init()`.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> Objeto</span>} objeto JSON com dados de localização. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-localization.md" format="dita" scope="local"> Localização dos elementos da interface do usuário</a> para obter mais informações. </p> <p>Consulte também o <i>Guia do usuário do SDK do visualizador</i> e o exemplo para obter mais informações sobre o conteúdo do objeto. </p> </td> 
  </tr> 
 </tbody> 
</table>

Consulte também [init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"PanLeftButton.TOOLTIP":"Left"},"fr":{"PanLeftButton.TOOLTIP":"Gauchiste"},defaultLocale:"en"})
```

