---
title: setHandlers
description: Referência da API do JavaScript para o eCatalog Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: a6709da7-1fa2-421b-8c99-a4ccea83c600
TQID: 'https://experienceleague.adobe.com/-ynEz2ykVWTs-kkCN760h-FnxpwM3JJidSL8WJseG6U'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 87
ht-degree: 0%

---

# setHandlers{#sethandlers}

Referência da API do JavaScript para o eCatalog Viewer.

`setHandlers(handlers)`

Especifica zero ou mais manipuladores de retorno de chamada. Uma chamada para esse método substitui totalmente os manipuladores de eventos atribuídos anteriormente para essa instância do visualizador. Deve ser chamado antes de `init()`.

## Parâmetro {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> manipuladores </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> objeto JSON com retornos de chamada de evento do visualizador, em que o nome da propriedade é o nome do evento do visualizador suportado e o valor da propriedade é uma referência de função JavaScript para um retorno de chamada apropriado. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-event-callbacks.md#concept-0bf5ff877043468db58ac62a92d002b6" format="dita" scope="local"> retornos de chamada de evento </a> para obter mais informações sobre eventos do visualizador. </p> </td> 
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
