---
description: Referência da API JavaScript para o eCatalog Viewer.
seo-description: Referência da API JavaScript para o eCatalog Viewer.
seo-title: setParam
solution: Experience Manager
title: setParam
topic: Dynamic Media
uuid: a732461f-1b34-4ebe-9dfd-69175762e574
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---


# setParam{#setparam}

Referência da API JavaScript para o eCatalog Viewer.

[!DNL ` setParam( *`nome, valor`*)`]

Define o parâmetro do visualizador para um valor especificado. O parâmetro é uma opção de configuração específica do visualizador ou um modificador do kit de desenvolvimento de software. Esse parâmetro é chamado antes de [!DNL `init()`].

Esse método é opcional se as informações de configuração do visualizador forem passadas com o objeto [!DNL `config`] JSON para o construtor.

Consulte também [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

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
[!DNL <instance>.setParam("style", "customStyle.css")]
```

