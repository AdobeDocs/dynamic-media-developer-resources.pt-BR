---
title: setParams
description: Referência da API do JavaScript para o Visualizador do carrossel.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 4bf3f8f8-73fe-4ab1-8005-aa49e4ffaba6
source-git-commit: 96ac67e5645c2c55920cc971806ba2f14ae57044
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# setParams{#setparams}

Referência da API do JavaScript para o Visualizador do carrossel.

` setParams( *`parâmetros`*)`

Define um ou mais parâmetros para um determinado valor. A sintaxe do argumento do método é idêntica a uma string de consulta de URL. Ou seja, ele representa pares name=value separados por `&`. Como em uma sequência de consulta, os nomes e os valores são codificados por porcentagem usando UTF8. Antes de chamar `init()`, esse parâmetro deve ser chamado.

Este método é opcional se as informações de configuração do visualizador foram passadas com o objeto JSON `config` para o construtor.

Consulte também [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Parâmetro {#section-add05f3d7ca0426897bd74bf7ac9b9cd}

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
<instance>.setParams("CarouselView.fmt=png&CarouselView.iscommand=op_sharpen%3d1")
```
