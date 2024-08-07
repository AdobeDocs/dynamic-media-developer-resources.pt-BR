---
title: setAsset
description: Referência da API do JavaScript para o Visualizador de mídia mista.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 3ad78de9-17a6-40c9-b389-a1f7eed11635
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# setAsset{#setasset}

Referência da API do JavaScript para o Visualizador de mídia mista.

` setAsset( *`ativo`*[,data]))`

Define o novo ativo e os dados adicionais opcionais do ativo. Você pode chamar este parâmetro a qualquer momento, antes ou depois de `init()`. Se for chamado depois de `init()`, o visualizador trocará o ativo no tempo de execução.

Consulte também [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Parâmetros {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`ativo`*` - { `String`} nova ID de ativo ou conjunto de mídia mista explícito, com modificadores opcionais do Servidor de imagens anexados após `?`.

Imagens que usam IR (Renderização de Imagem) ou UGC (Conteúdo Gerado pelo Usuário) não são compatíveis com esse visualizador.

`*`dados`*` - { `JSON`} local do novo arquivo de legenda.

Se não for especificado, o botão de legenda não ficará visível na interface. As legendas especificadas com esse parâmetro se aplicam ao vídeo que vem primeiro no conjunto de mídias mistas; os vídeos subsequentes são reproduzidos sem legendas. Esse visualizador é compatível com as seguintes IDs de componente:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ID do componente </p> </th> 
   <th colname="col2" class="entry"> <p>Nome da classe do componente do visualizador do SDK </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posterimage </span> </p> </td> 
   <td colname="col2"> <p>Imagem a ser exibida no primeiro quadro antes do início da reprodução do vídeo. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-posterimage.md#reference-f424ad0f278b4d14b86ea55e3a73c52b" format="dita" scope="local"> VideoPlayer.posterimage </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Legenda <span class="codeph"> </span> </p> </td> 
   <td colname="col2"> <p> Local do novo arquivo de legenda. </p> <p>Se não for especificado, o botão de legenda não ficará visível na interface. As legendas especificadas com esse parâmetro se aplicam ao vídeo que aparece primeiro no conjunto de mídias. Os vídeos subsequentes são reproduzidos sem legendas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referência do conjunto de mídia única:

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample")
```

Conjunto de mídia explícito:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;")
```

Modificador de nitidez adicionado a todas as imagens do conjunto:

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample?op_sharpen=1")
```
