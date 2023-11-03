---
title: setAsset
description: Referência da API JavaScript para o Visualizador de vídeo interativo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 24d8d11d-4688-4ca0-92ae-824a5e984a10
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# setAsset{#setasset}

Referência da API JavaScript para o Visualizador de vídeo interativo.

`setAsset(asset[, data])`

Define o novo ativo e os dados adicionais opcionais do ativo. Você pode chamar esse parâmetro a qualquer momento, antes ou depois de `init()`. Se for chamado depois de `init()`, o visualizador troca o ativo no tempo de execução.

Consulte também [init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ativo </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>} ID do novo ativo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dados </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> JSON </span>} objeto JSON com os seguintes campos opcionais (diferencia maiúsculas de minúsculas): </p> <p> 
     <ul id="ul_924FB99ACF0F43699CD229593F1C1384"> 
      <li id="li_F3CFEF28BCB7450991EFE0BD4EB28E36"> <span class="codeph"> posterimage </span> - Imagem a ser exibida no primeiro quadro antes do início da reprodução do vídeo. Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-videoplayer-posterimage.md#reference-8e8e2b3e7e9c4ee8b6dadf90cef494f7" format="dita" scope="local"> VideoPlayer.posterimage </a>. </li> 
      <li id="li_D6C3E543C70942C582020780E2DF74C8"> <span class="codeph"> legenda </span> - local do novo arquivo de legenda. Se não for especificado, o botão de legenda não ficará visível na interface. </li> 
      <li id="li_BF866BD7275E450EA08A0E72FAA9D3AE"> <span class="codeph"> navegação </span> - URL ou caminho para o conteúdo de navegação WebVTT. O arquivo WebVTT deve ser fornecido pelo Servidor de imagens. </li> 
      <li id="li_0C0EC5AB00554EC6AA01F60684A40213"> <span class="codeph"> interativeData </span> - URL ou caminho para o conteúdo de dados interativos de WebVTT. O arquivo WebVTT deve ser fornecido pelo Servidor de imagens. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4")
```
