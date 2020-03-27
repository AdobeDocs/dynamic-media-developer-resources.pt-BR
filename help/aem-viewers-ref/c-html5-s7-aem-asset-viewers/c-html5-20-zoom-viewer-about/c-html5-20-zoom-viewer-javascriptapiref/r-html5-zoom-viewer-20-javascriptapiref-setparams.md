---
description: Referência da API JavaScript para o Visualizador de vídeo.
seo-description: Referência da API JavaScript para o Visualizador de vídeo.
seo-title: setParams
solution: Experience Manager
title: setParams
topic: Dynamic media
uuid: 2f431747-df81-49ed-b323-c70080883c8a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setParams{#setparams}

Referência da API JavaScript para o Visualizador de vídeo.

` setParams( *`params`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value pares de parâmetros separados por <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Define um ou mais parâmetros para um determinado valor. A sintaxe do argumento de método é idêntica a uma string de query de URL. Ou seja, representa pares de nome=valor separados por `&`. Assim como em uma string de query, os nomes e valores são codificados por porcentagem usando UTF8. Antes de chamar `init()`, esse parâmetro deve ser chamado.

Esse método é opcional se as informações de configuração do visualizador forem passadas com o objeto `config` JSON para o construtor.

Consulte também [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("ZoomView.zoomfactor=2,3&ZoomView.iscommand=op_sharpen%3d1")
```

