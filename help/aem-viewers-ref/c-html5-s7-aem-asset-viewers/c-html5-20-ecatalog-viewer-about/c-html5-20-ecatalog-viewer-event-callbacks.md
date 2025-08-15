---
title: Retornos de chamada de evento
description: Retornos de chamada de evento
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 7bd2e167-d04c-43e2-a71c-e2b3dddb13a0
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '147'
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
   * `eventInfo {String}` carga do evento

Consulte também [eCatalogViewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-ecatalogviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) e [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-sethandlers.md#reference-7858574ff5c34ce993ef4fdff741a856).
