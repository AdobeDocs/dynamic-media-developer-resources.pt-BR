---
description: Retornos de chamada de evento
solution: Experience Manager
title: Retornos de chamada de evento
topic: Dynamic Media
uuid: 325a3ccf-bae9-46f6-b3d0-70041a9548bb
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# Retornos de chamada do evento{#event-callbacks}

O visualizador suporta retornos de chamada do evento JavaScript que a página da Web usa para rastrear o processo de inicialização do visualizador ou o comportamento do tempo de execução.

Os manipuladores de retorno de chamada são atribuídos transmitindo nomes de eventos e funções de manipulador correspondentes com a propriedade `handlers` para o objeto JSON `config` no construtor do visualizador. Como alternativa, é possível usar o método da API `setHandlers()`.

Os eventos do visualizador suportados incluem:

* `initComplete` - dispara quando a inicialização do visualizador é concluída e todos os componentes internos são criados, para que seja possível usar a  `getComponent()` API. O manipulador de retorno de chamada não aceita nenhum argumento.

* `trackEvent` - dispara cada vez que um evento ocorre dentro do visualizador que pode ser manipulado por um sistema de rastreamento de eventos, como o Adobe Analytics. O manipulador de retorno de chamada aceita os seguintes argumentos:

   * `objID {String}` não utilizado no momento.
   * `compClass {String}` não utilizado no momento.
   * `instName {String}` um nome de instância do componente SDK do visualizador que acionou o evento.
   * `timeStamp {Number}` evento carimbo de data/hora.
   * `eventInfo {String}` Carga do evento.

Consulte também [ZoomViewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-zoomviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) e [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
