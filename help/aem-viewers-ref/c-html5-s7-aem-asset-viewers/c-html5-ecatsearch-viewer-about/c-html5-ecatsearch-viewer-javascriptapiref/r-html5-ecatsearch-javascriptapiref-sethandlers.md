---
description: Referência da API JavaScript para o eCatalog Viewer.
seo-description: Referência da API JavaScript para o eCatalog Viewer.
seo-title: setHandlers
solution: Experience Manager
title: setHandlers
topic: Dynamic media
uuid: 602fbf82-429b-443c-9163-f4d2e2b922dd
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# setHandlers{#sethandlers}

Referência da API JavaScript para o eCatalog Viewer.

[!DNL `setHandlers(handlers)`]

Especifica zero ou mais manipuladores de retorno de chamada. Uma chamada para esse método substitui totalmente os manipuladores de eventos que foram atribuídos anteriormente para essa instância do visualizador. Deve ser chamado antes `init()`.

## Parâmetro {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> manipuladores </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> Objeto JSON {Object} </span> com retornos de chamada de evento do visualizador, onde o nome da propriedade é o nome do evento do visualizador suportado e o valor da propriedade é uma referência de função JavaScript para um retorno de chamada apropriado. </p> <p>Consulte Retornos de chamada do <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-event-callbacks.md#concept-0bf5ff877043468db58ac62a92d002b6" format="dita" scope="local"> Evento </a> para obter mais informações sobre eventos do visualizador. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```

