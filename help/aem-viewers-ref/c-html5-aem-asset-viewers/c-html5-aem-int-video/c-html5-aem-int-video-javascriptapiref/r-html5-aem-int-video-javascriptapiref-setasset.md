---
description: Referência da API JavaScript para o Visualizador de vídeo interativo.
seo-description: Referência da API JavaScript para o Visualizador de vídeo interativo.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: 80c670a4-1251-47f5-a66b-8ba5019df1ce
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# setAsset{#setasset}

Referência da API JavaScript para o Visualizador de vídeo interativo.

`setAsset(asset[, data])`

Define o novo ativo e os dados opcionais do ativo adicional. Você pode chamar esse parâmetro a qualquer momento, antes ou depois `init()`. Se for chamado depois `init()`, o visualizador alterna o ativo em tempo de execução.

Consulte também [init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ativo </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>} nova ID de ativo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> data </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> JSON </span>} objeto JSON com os seguintes campos opcionais (diferencia maiúsculas de minúsculas): </p> <p> 
     <ul id="ul_924FB99ACF0F43699CD229593F1C1384"> 
      <li id="li_F3CFEF28BCB7450991EFE0BD4EB28E36"> <span class="codeph"> posterimage </span> - imagem a ser exibida no primeiro quadro antes da reprodução dos start de vídeo. Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-videoplayer-posterimage.md#reference-8e8e2b3e7e9c4ee8b6dadf90cef494f7" format="dita" scope="local"> VideoPlayer.posterimage </a>. </li> 
      <li id="li_D6C3E543C70942C582020780E2DF74C8"> <span class="codeph"> caption </span> - local do novo arquivo de legenda. Se não for especificado, o botão de legenda não estará visível na interface do usuário. </li> 
      <li id="li_BF866BD7275E450EA08A0E72FAA9D3AE"> <span class="codeph"> navigation </span> - URL ou caminho para o conteúdo de navegação WebVTT. O arquivo WebVTT deve ser servido pelo Serviço de Imagens. </li> 
      <li id="li_0C0EC5AB00554EC6AA01F60684A40213"> <span class="codeph"> interativeData </span> - URL ou caminho para o conteúdo de dados interativos WebVTT. O arquivo WebVTT deve ser servido pelo Serviço de Imagens. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4")
```

