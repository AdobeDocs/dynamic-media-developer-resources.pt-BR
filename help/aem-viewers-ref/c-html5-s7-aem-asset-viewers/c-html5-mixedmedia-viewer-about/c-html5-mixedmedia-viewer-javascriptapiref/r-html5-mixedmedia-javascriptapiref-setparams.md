---
description: Referência da API do JavaScript para o Visualizador de mídia mista.
seo-description: Referência da API do JavaScript para o Visualizador de mídia mista.
seo-title: setParams
solution: Experience Manager
title: setParams
uuid: 46db0ce3-fd70-4577-92ed-e7d2d15e0dab
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídias mistas
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# setParams{#setparams}

Referência da API do JavaScript para o Visualizador de mídia mista.

` setParams( *`params`*)`

Define um ou mais parâmetros para um determinado valor. A sintaxe do argumento do método é idêntica a uma string de consulta de URL. Ou seja, representa pares name=value separados por `&`. Assim como em uma sequência de consulta, os nomes e valores são codificados por porcentagem usando UTF8. Antes de chamar `init()`, esse parâmetro deve ser chamado. Esse método é opcional se as informações de configuração do visualizador forem passadas com `config` objeto JSON para o construtor.

Consulte também [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value parâmetros pares separados por  <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("ZoomView.zoomstep=2,3&ZoomView.iscommand=op_sharpen%3d1")
```

