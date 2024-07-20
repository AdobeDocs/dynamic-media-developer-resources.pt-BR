---
title: setParams
description: Referência da API do JavaScript para o Visualizador de zoom básico.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f142dd72-5e45-44f6-a79b-3eaf6a310bde
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# setParams{#setparams}

Referência da API do JavaScript para o Visualizador de zoom básico.

` setParams( *`parâmetros`*)`

Define um ou mais parâmetros para um determinado valor. A sintaxe do argumento do método é idêntica a uma string de consulta de URL. Ou seja, ele representa pares name=value separados por `&`. Como em uma sequência de consulta, os nomes e os valores são codificados por porcentagem usando UTF8. Antes de chamar `init()`, esse parâmetro deve ser chamado.

Este método é opcional se as informações de configuração do visualizador foram passadas com o objeto JSON `config` para o construtor.

Consulte também [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> parâmetros</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> pares de parâmetros name=value separados por <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("ZoomView.zoomfactor=2,3&ZoomView.iscommand=op_sharpen%3d1")
```
