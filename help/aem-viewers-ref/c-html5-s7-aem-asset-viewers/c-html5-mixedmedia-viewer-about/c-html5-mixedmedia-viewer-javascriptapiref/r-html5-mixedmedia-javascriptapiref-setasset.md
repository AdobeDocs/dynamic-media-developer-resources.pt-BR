---
description: Referência da API do JavaScript para o Visualizador de mídia mista.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídias mistas
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---


# setAsset{#setasset}

Referência da API do JavaScript para o Visualizador de mídia mista.

` setAsset( *`ativo`*[,data]))`

Define o novo ativo e os dados opcionais do ativo adicional. Você pode chamar esse parâmetro a qualquer momento, antes ou depois de `init()`. Se for chamado depois de `init()`, o visualizador troca o ativo no tempo de execução.

Consulte também [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Parâmetros {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`asset`*`  - {  `String`} nova ID de ativo ou conjunto de mídia mista explícito, com modificadores opcionais de Exibição de imagem anexados após  `?`.

As imagens que usam IR (Renderização de imagem) ou UGC (Conteúdo gerado pelo usuário) não são suportadas por esse visualizador.

`*`data`*`  - {  `JSON`} local do novo arquivo de legenda.

Se não for especificado, o botão de legenda não estará visível na interface do usuário. As legendas especificadas com esse parâmetro aplicam-se ao vídeo que vem primeiro no conjunto de mídias mistas; os vídeos subsequentes são reproduzidos sem legendas. Esse visualizador é compatível com as seguintes IDs de componente:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ID do componente </p> </th> 
   <th colname="col2" class="entry"> <p>Nome da classe do componente SDK do visualizador </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posterimage  </span> </p> </td> 
   <td colname="col2"> <p>Imagem a ser exibida no primeiro quadro antes da reprodução do vídeo. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-posterimage.md#reference-f424ad0f278b4d14b86ea55e3a73c52b" format="dita" scope="local"> VideoPlayer.posterimage </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> caption  </span> </p> </td> 
   <td colname="col2"> <p> Localização do novo arquivo de legenda. </p> <p>Se não for especificado, o botão de legenda não estará visível na interface do usuário. As legendas especificadas com esse parâmetro aplicam-se ao vídeo que vem primeiro no conjunto de mídia. Os vídeos subsequentes são reproduzidos sem legendas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referência do conjunto de mídia única:

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample")
```

Conjunto de mídias explícito:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;")
```

Modificador de nitidez adicionado a todas as imagens no conjunto:

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample?op_sharpen=1")
```

