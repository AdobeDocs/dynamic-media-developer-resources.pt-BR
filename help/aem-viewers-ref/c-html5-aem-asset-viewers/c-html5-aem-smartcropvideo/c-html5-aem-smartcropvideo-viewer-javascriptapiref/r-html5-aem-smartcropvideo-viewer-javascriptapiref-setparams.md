---
title: setParams
description: Referência da API do JavaScript para o visualizador de vídeo de recorte inteligente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 76bad894-bfb8-4d79-b3ff-c2497c68e5e8
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# setParams{#setparams}

Referência da API do JavaScript para o visualizador de vídeo de recorte inteligente.

` setParams( *`params`*)`

Define um ou mais parâmetros para um determinado valor. A sintaxe do argumento do método é idêntica a uma string de consulta de URL. Ou seja, representa pares name=value separados por `&`. O mesmo que em uma sequência de consulta, nomes e valores é codificado por porcentagem usando UTF8. Antes de chamar `init()`, esse parâmetro deve ser chamado.

Esse método é opcional se as informações de configuração do visualizador forem passadas com `config` Objeto JSON para o construtor.

Consulte também [init](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> pares de parâmetros name=value separados por <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("style=customStyle.css&SmartCropVideoPlayer.playback=progressive")
```
