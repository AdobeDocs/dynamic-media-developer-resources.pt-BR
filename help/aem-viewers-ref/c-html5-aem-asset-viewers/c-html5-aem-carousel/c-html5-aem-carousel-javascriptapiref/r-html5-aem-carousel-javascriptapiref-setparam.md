---
description: Referência da API JavaScript para o Visualizador do carrossel.
seo-description: Referência da API JavaScript para o Visualizador do carrossel.
seo-title: setParam
solution: Experience Manager
title: setParam
topic: Dynamic Media
uuid: 87f16ea9-0267-4114-9aeb-a68fdb616a88
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---


# setParam{#setparam}

Referência da API JavaScript para o Visualizador do carrossel.

` setParam( *`nome, valor`*)`

Define o parâmetro do visualizador para um valor especificado. O parâmetro é uma opção de configuração específica do visualizador ou um modificador do kit de desenvolvimento de software. Esse parâmetro é chamado antes de `init()`.

Esse método é opcional se as informações de configuração do visualizador forem passadas com o objeto `config` JSON para o construtor.

Consulte também [xref](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md).

## Parâmetros {#section-c68a5a3688d342fd9d6a7fd59867cc7a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}  </span> nome do parâmetro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}  </span> valor do parâmetro. O valor não pode ser codificado por porcentagem. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "etc/dam/presets/css/html5_carouselviewer_dotted_light.css")
```

