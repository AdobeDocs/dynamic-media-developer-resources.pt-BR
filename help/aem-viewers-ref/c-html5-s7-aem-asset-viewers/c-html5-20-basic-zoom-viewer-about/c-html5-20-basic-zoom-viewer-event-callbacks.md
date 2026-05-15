---
title: Retornos de chamada de evento
description: Retornos de chamada de evento
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 14b317ab-82fb-4f55-babe-72c24e6afc2c
TQID: 'https://experienceleague.adobe.com/GEH2LfIdpNqG-PuOObYC0BHtfetkMJDIf32HCEmP9u4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 147
ht-degree: 0%

---

# Retornos de chamada de evento{#event-callbacks}

O visualizador suporta retornos de chamada de evento do JavaScript que a página da Web usa para rastrear o processo de inicialização do visualizador ou o comportamento do tempo de execução.

Os manipuladores de retorno de chamada são atribuídos passando nomes de evento e funções de manipulador correspondentes com a propriedade `handlers` para o objeto JSON `config` no construtor do visualizador. Como alternativa, é possível usar o método da API `setHandlers()`.

Os eventos do visualizador compatíveis incluem o seguinte:

* `initComplete` - acionado quando a inicialização do visualizador é concluída e todos os componentes internos são criados, para que seja possível usar a API `getComponent()`. O manipulador de retorno de chamada não aceita argumentos.

* `trackEvent` - acionado cada vez que um evento ocorre dentro do visualizador, o qual pode ser manipulado por um sistema de rastreamento de eventos, como o Adobe Analytics. O manipulador de retorno de chamada usa os seguintes argumentos:

   * `objID {String}` não usado atualmente.
   * `compClass {String}` não usado atualmente.
   * `instName {String}` um nome de instância do componente SDK do Visualizador que acionou o evento.
   * Carimbo de data/hora do evento `timeStamp {Number}`.
   * `eventInfo {String}` carga do evento.

Consulte também [BasicZoomViewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-basiczoomviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) e [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-sethandlers.md#reference-b748b29eaafa463a9d1723cb7b86f0d9).
