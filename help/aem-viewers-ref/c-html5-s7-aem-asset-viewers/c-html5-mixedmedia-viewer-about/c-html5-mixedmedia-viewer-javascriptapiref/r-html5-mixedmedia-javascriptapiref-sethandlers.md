---
description: Referência da API do JavaScript para o Visualizador de mídia mista.
solution: Experience Manager
title: setHandlers
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídias mistas
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# setHandlers{#sethandlers}

Referência da API do JavaScript para o Visualizador de mídia mista.

`setHandlers(handlers)`

Especifica zero ou mais manipuladores de retorno de chamada. Uma chamada para esse método substitui totalmente os manipuladores de eventos que foram atribuídos anteriormente para essa instância do visualizador. Deve ser chamado antes de `init()`.

## Parâmetro {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> manipuladores  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> Objeto  </span> JSON {Object} com retornos de chamada do evento do visualizador, em que o nome da propriedade é o nome do evento do visualizador suportado e o valor da propriedade é uma referência de função JavaScript para um retorno de chamada apropriado. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-event-callbacks.md#concept-273d2cddbb7144e284b618ffaf3deabc" format="dita" scope="local"> Retornos de chamada do evento </a> para obter mais informações sobre os eventos do visualizador. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```

