---
title: setHandlers
description: Referência da API do JavaScript para o visualizador de vídeo
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: cff331a9-bca1-4360-88fa-96812aa8ba62
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---

# setHandlers{#sethandlers}

Referência da API do JavaScript para o visualizador de vídeo

`setHandlers(handlers)`

Especifica zero ou mais manipuladores de retorno de chamada. Uma chamada para esse método substitui totalmente os manipuladores de eventos atribuídos anteriormente para essa instância do visualizador. Deve ser chamado antes de `init()`.

## Parâmetro {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> manipuladores </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> objeto JSON com retornos de chamada do evento do visualizador, em que o nome da propriedade é o nome do evento do visualizador com suporte e o valor da propriedade é uma referência de função JavaScript para um retorno de chamada apropriado. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> retornos de chamada de evento </a> para obter mais informações sobre eventos do visualizador. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```
