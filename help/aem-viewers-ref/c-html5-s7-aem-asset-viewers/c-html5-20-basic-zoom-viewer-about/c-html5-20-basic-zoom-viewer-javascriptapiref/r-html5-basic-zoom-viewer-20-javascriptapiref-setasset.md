---
description: Referência da API JavaScript para Visualizador de zoom básico.
seo-description: Referência da API JavaScript para Visualizador de zoom básico.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic Media
uuid: af433f15-34a0-4867-97c5-acab47e3e008
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---


# setAsset{#setasset}

Referência da API JavaScript para Visualizador de zoom básico.

` setAsset( *`ativo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ativo</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} nova ID de ativo, com modificadores IS opcionais anexados após "?" </p> <p> As imagens que usam IR (Renderização de imagem) ou UGC (Conteúdo gerado pelo usuário) não são suportadas por este visualizador. </p> </td> 
  </tr> 
 </tbody> 
</table>

Define o novo ativo. Você pode chamar esse parâmetro a qualquer momento, antes ou depois de `init()`. Se for chamado depois de `init()`, o visualizador alternará o ativo em tempo de execução.

Consulte também [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referência de imagem única:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

Modificador de nitidez adicionado a todas as imagens no conjunto:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B?op_sharpen=1")
```

