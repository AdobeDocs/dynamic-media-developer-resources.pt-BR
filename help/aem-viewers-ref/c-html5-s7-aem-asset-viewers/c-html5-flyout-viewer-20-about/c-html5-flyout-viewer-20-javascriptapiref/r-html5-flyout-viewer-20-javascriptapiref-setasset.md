---
title: setAsset
description: Referência da API do JavaScript para o Visualizador de submenu.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: cd66267e-7b25-4af4-b83c-f7b7f768ea8c
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# setAsset{#setasset}

Referência da API do JavaScript para o Visualizador de submenu.

` setAsset( *`ativo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ativo</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> Cadeia de caracteres</span>} nova ID de ativo, conjunto de imagens explícitas, ou conjunto de imagens explícitas com modificadores de Servidor de imagens específicos de quadro, com modificadores de Servidor de imagens globais opcionais anexados após <span class="codeph"> ?</span>. </p> <p> Imagens que usam IR (Renderização de Imagem) ou UGC (Conteúdo Gerado pelo Usuário) não são compatíveis com esse visualizador. </p> </td> 
  </tr> 
 </tbody> 
</table>

Define o novo ativo. Você pode chamar este parâmetro a qualquer momento, antes ou depois de `init()`. Se for chamado depois de `init()`, o visualizador trocará o ativo no tempo de execução.

Consulte também [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referência de imagem única:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

Referência única a um conjunto de imagens definido em um catálogo:

```
<instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

Conjunto de imagens explícito da seguinte maneira:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

Conjunto de imagens explícito com modificadores do Servidor de imagens específicos do quadro:

```
<instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

Modificador de nitidez adicionado a todas as imagens do conjunto:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C?op_sharpen=1")
```
