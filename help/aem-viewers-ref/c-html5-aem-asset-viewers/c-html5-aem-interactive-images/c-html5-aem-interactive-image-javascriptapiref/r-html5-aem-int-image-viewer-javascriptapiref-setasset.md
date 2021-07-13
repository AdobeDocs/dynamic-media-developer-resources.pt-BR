---
description: Referência da API do JavaScript para o Visualizador de imagem de vídeo.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Visualizadores,SDK/API,Imagens interativas
role: Developer,User
exl-id: e5f88bc9-a880-45eb-9554-57e185937d29
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---

# setAsset{#setasset}

Referência da API do JavaScript para o Visualizador de imagem de vídeo.

` setAsset( *`ativo`*)`

Define o novo ativo. Você pode chamar esse parâmetro a qualquer momento, antes ou depois de `init()`. Se for chamado depois de `init()`, o visualizador troca o ativo no tempo de execução.

Consulte também [init](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ativo</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} nova ID de ativo. </p> <p>As imagens que usam IR (Renderização de imagem) ou UGC (Conteúdo gerado pelo usuário) não são suportadas por esse visualizador. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Referência de imagem única:

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg")
```
