---
description: nulo
seo-description: nulo
seo-title: Retornos de chamada de Evento
solution: Experience Manager
title: Retornos de chamada de Evento
topic: Dynamic media
uuid: 1b9af9e4-463a-4982-9e81-681ebebfd6d7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

Consulte também [BasicZoomViewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-basiczoomviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) e [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-sethandlers.md#reference-b748b29eaafa463a9d1723cb7b86f0d9).
