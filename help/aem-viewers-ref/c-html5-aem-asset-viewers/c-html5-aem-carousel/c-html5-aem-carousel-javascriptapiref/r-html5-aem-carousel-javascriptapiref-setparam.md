---
title: setParam
description: Referência da API do JavaScript para o Visualizador do carrossel.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 0829933f-a90b-4066-9904-748f2a727169
source-git-commit: 96ac67e5645c2c55920cc971806ba2f14ae57044
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# setParam{#setparam}

Referência da API do JavaScript para o Visualizador do carrossel.

` setParam( *`nome, valor`*)`

Define o parâmetro do visualizador para um valor especificado. O parâmetro é uma opção de configuração específica do visualizador ou um modificador do kit de desenvolvimento de software. Este parâmetro é chamado antes de `init()`.

Este método é opcional se as informações de configuração do visualizador foram passadas com o objeto JSON `config` para o construtor.

Consulte também [xref](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md).

## Parâmetros {#section-c68a5a3688d342fd9d6a7fd59867cc7a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> nome </span> </span> </p> </td>
   <td colname="col2"> <p> <span class="codeph"> {string} </span> nome do parâmetro. </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> valor </span> </span> </p> </td>
   <td colname="col2"> <p> <span class="codeph"> {string} </span> valor do parâmetro. O valor não pode ser codificado por porcentagem. </p> </td>
  </tr>
 </tbody>
</table>

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "etc/dam/presets/css/html5_carouselviewer_dotted_light.css")
```
