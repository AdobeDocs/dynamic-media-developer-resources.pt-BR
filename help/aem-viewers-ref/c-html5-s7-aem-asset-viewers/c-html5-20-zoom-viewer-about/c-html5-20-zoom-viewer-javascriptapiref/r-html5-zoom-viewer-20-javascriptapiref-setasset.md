---
title: setAsset
description: Referência da API do JavaScript para o Visualizador de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 4fc94f30-e330-4c8a-b6da-d870e4f8e4ab
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# setAsset{#setasset}

Referência da API do JavaScript para o Visualizador de vídeo.

` setAsset( *`ativo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ativo </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> Cadeia de caracteres </span>} nova ID do ativo, conjunto de imagens explícitas, ou conjunto de imagens explícitas com modificadores do Servidor de imagens específicos do quadro, com modificadores opcionais do Servidor de imagens globais anexados após "?". </p> <p> Imagens que usam IR (Renderização de Imagem) ou UGC (Conteúdo Gerado pelo Usuário) não são compatíveis com esse visualizador. </p> </td> 
  </tr> 
 </tbody> 
</table>

Define o novo ativo. Você pode chamar este parâmetro a qualquer momento, antes ou depois de `init()`. Se for chamado depois de `init()`, o visualizador trocará o ativo no tempo de execução.

Consulte também [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referência de imagem única como a seguir:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

Referência única a um conjunto de imagens definido em um catálogo da seguinte maneira:

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

Conjunto de imagens explícito da seguinte maneira:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

Conjunto de imagens explícito com modificadores do Servidor de imagens específicos do quadro, da seguinte maneira:

```
 <instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

O modificador de nitidez foi adicionado a todas as imagens no conjunto da seguinte maneira:

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample?op_sharpen=1")
```
