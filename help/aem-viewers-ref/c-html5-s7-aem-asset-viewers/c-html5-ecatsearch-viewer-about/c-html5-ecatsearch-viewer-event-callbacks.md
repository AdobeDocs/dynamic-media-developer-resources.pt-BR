---
description: nulo
seo-description: nulo
seo-title: Retornos de chamada de Evento
solution: Experience Manager
title: Retornos de chamada de Evento
topic: Dynamic media
uuid: 0c4c4111-5ad7-458c-afa2-d551b5987322
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# Retornos de chamada de Evento{#event-callbacks}

O visualizador suporta retornos de chamada do evento JavaScript que a página da Web usa para rastrear o processo de inicialização do visualizador ou o comportamento do tempo de execução.

Os manipuladores de retorno de chamada são atribuídos transmitindo nomes de eventos e funções de manipulador correspondentes com a `handlers` propriedade para o objeto `config` JSON no construtor do visualizador. Como alternativa, é possível usar o método `setHandlers()` API.

Os eventos do visualizador suportados incluem:

* `initComplete` - aciona quando a inicialização do visualizador é concluída e todos os componentes internos são criados, para que seja possível usar a `getComponent()` API. O manipulador de retorno de chamada não aceita nenhum argumento.

* `trackEvent` - dispara cada vez que um evento ocorre dentro do visualizador que pode ser manipulado por um sistema de rastreamento de eventos, como o Adobe Analytics. O manipulador de retorno de chamada aceita os seguintes argumentos:

   * `objID {String}` não utilizado no momento.
   * `compClass {String}` não utilizado no momento.
   * `instName {String}` um nome de instância do componente SDK do visualizador que acionou o evento.
   * `timeStamp {Number}` evento carimbo de data/hora.
   * `eventInfo {String}` Carga do evento.

Consulte também [eCatalogViewer](/help/aem-viewers-ref/c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-javascriptapiref/r-html5-ecatsearch-javascriptapiref-ecatalogsearchviewer.md) e [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-sethandlers.md#reference-7858574ff5c34ce993ef4fdff741a856).
