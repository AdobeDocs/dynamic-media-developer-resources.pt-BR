---
description: Referência da API JavaScript para o Visualizador de imagens interativo
seo-description: Referência da API JavaScript para o Visualizador de imagens interativo
seo-title: setHandlers
solution: Experience Manager
title: setHandlers
topic: Dynamic media
uuid: 93db9c88-890e-4be8-b82f-d15978a0cfac
translation-type: tm+mt
source-git-commit: 323a4f72b5bb46832a569ffad38104bac7da17df
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---


# setHandlers{#sethandlers}

Referência da API JavaScript para o Visualizador de imagens interativo

`setHandlers(handlers)`

Especifica zero ou mais manipuladores de retorno de chamada. Uma chamada para esse método substitui totalmente os manipuladores de eventos que foram atribuídos anteriormente para essa instância do visualizador. Deve ser chamado antes `init()`.

## Parâmetro {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> manipuladores </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> Objeto JSON {Object} </span> com retornos de chamada de evento do visualizador. O nome da propriedade é o nome do evento do visualizador suportado. O valor da propriedade é uma referência de função JavaScript para um retorno de chamada apropriado. </p> <p>Consulte Retornos de chamada do <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Evento </a> para obter mais informações sobre eventos do visualizador. </p> </td> 
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

