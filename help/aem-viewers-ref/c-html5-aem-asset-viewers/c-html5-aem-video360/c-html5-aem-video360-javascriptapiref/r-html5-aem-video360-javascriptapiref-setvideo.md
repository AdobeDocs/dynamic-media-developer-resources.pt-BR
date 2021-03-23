---
description: Referência da API do JavaScript para o visualizador do Video360
seo-description: Referência da API do JavaScript para o visualizador do Video360
seo-title: setVideo
solution: Experience Manager
title: setVideo
uuid: 749aa32c-c27f-476c-954b-d4524528bccc
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo 360 VR
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 0%

---


# setVideo{#setvideo}

Referência da API do JavaScript para o visualizador do Video360

`setVideo(videoUrl)`

Define o novo vídeo externo. Pode ser chamado a qualquer momento, antes e depois de `init()`. Se chamado depois de `init()`, o visualizador troca o vídeo em tempo de execução.

Consulte também [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## Parâmetros {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl  </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> Cadeia de caracteres</span>} é um URL absoluto para o novo vídeo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setVideo("https://s7d9.scene7.com/is/content/Viewers/space_station_360")
```

