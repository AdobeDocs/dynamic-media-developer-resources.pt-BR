---
description: Referência da API JavaScript para o Visualizador de vídeo.
seo-description: Referência da API JavaScript para o Visualizador de vídeo.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: b95cef30-41ad-47d5-b0f1-efc8831c7bdc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAsset{#setasset}

Referência da API JavaScript para o Visualizador de vídeo.

` setAsset( *`ativo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ativo </span></span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>} nova ID de ativo ou conjunto de imagens explícito com modificadores opcionais do Serviço de imagens anexados após <span class="codeph"> ? </span>. </p> <p> As imagens que usam IR (Renderização de imagem) ou UGC (Conteúdo gerado pelo usuário) não são suportadas por este visualizador. </p> </td> 
  </tr> 
 </tbody> 
</table>

Define um novo ativo. Você pode chamar esse parâmetro a qualquer momento, antes ou depois `init()`. Se for chamado depois `init()`, o visualizador alterna o ativo em tempo de execução.

Consulte também [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referência única para um conjunto de imagens definido em um catálogo:

```
 <instance>.setAsset("Viewers/Pluralist")
```

Conjunto de imagens explícito, com páginas pré-combinadas:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C,Scene7SharedAssets/Backpack_H,Scene7SharedAssets/Backpack_J")
```

Conjunto de imagens explícito, com imagens de página individuais:

```
 <instance>.setAsset("Scene7SharedAssets/AdobeScene7_Overview_US-1,Scene7SharedAssets/AdobeScene7_Overview_US-2:AdobeScene7_Overview_US-3,Scene7SharedAssets/AdobeScene7_Overview_US-4")
```

Modificador de nitidez adicionado a todas as imagens no conjunto:

```
 <instance>.setAsset("Viewers/Pluralist?op_sharpen=1")
```

