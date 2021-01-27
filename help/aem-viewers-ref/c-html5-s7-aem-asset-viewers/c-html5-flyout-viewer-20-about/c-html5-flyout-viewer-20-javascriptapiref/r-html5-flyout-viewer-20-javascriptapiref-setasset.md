---
description: Referência da API JavaScript para Flyout Viewer.
seo-description: Referência da API JavaScript para Flyout Viewer.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic Media
uuid: c6f7e7e9-084a-46ff-8cff-1ecb71f7b8d3
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---


# setAsset{#setasset}

Referência da API JavaScript para Flyout Viewer.

` setAsset( *`ativo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ativo</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} nova ID de ativo, conjunto de imagens explícito ou conjunto de imagens explícito com modificadores de Serviço de Imagens específicos do quadro, com modificadores de Serviço de Imagens globais opcionais anexados após <span class="codeph"> ?</span>. </p> <p> As imagens que usam IR (Renderização de imagem) ou UGC (Conteúdo gerado pelo usuário) não são suportadas por este visualizador. </p> </td> 
  </tr> 
 </tbody> 
</table>

Define o novo ativo. Você pode chamar esse parâmetro a qualquer momento, antes ou depois de `init()`. Se for chamado depois de `init()`, o visualizador alternará o ativo em tempo de execução.

Consulte também [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referência de imagem única:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

Referência única para um conjunto de imagens definido em um catálogo:

```
<instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

Conjunto de imagens explícito:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

Conjunto de imagens explícito com modificadores do Servidor de imagens específicos do quadro:

```
<instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

Modificador de nitidez adicionado a todas as imagens no conjunto:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C?op_sharpen=1")
```

