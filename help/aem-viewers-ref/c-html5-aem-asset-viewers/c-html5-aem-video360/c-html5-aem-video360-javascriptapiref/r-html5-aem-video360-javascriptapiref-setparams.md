---
description: Referência da API do JavaScript para o visualizador do Video360.
seo-description: Referência da API do JavaScript para o visualizador do Video360.
seo-title: setParams
solution: Experience Manager
title: setParams
uuid: 0a5b9798-0e3f-4310-9b6e-0214a420951b
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo 360 VR
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---


# setParams{#setparams}

Referência da API do JavaScript para o visualizador do Video360.

` setParams( *`params`*)`

Define um ou mais parâmetros para um determinado valor. A sintaxe do argumento do método é idêntica a uma string de consulta de URL. Ou seja, representa pares name=value separados por `&`. Assim como em uma sequência de consulta, os nomes e valores são codificados por porcentagem usando UTF8. Antes de chamar `init()`, esse parâmetro deve ser chamado.

Esse método é opcional se as informações de configuração do visualizador foram passadas com `config` objeto JSON para o construtor.

Consulte também [init](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Parâmetro {#section-add05f3d7ca0426897bd74bf7ac9b9cd}

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
<instance>.setParams("style=customStyle.css&VideoPlayer.playback=progressive")
```

