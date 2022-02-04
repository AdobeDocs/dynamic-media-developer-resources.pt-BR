---
title: Retornos de chamada do evento
description: Retornos de chamada do evento
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1a7b51c1-baa7-4ae3-b6b7-17478055a605
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# Retornos de chamada do evento{#event-callbacks}

O visualizador suporta retornos de chamada de evento JavaScript que a página da Web usa para rastrear o processo de inicialização do visualizador ou o comportamento do tempo de execução.

Os manipuladores de chamada de retorno são atribuídos transmitindo os nomes de evento e as funções de manipulador correspondentes com o `handlers` propriedade para `config` Objeto JSON no construtor do visualizador. Como alternativa, é possível usar `setHandlers()` Método da API.

Os eventos compatíveis do visualizador incluem:

* `initComplete` - dispara quando a inicialização do visualizador é concluída e todos os componentes internos são criados, para que seja possível usar `getComponent()` API. O manipulador de retorno de chamada não aceita argumentos.

* `trackEvent` - dispara sempre que um evento ocorre no visualizador, o que pode ser manipulado por um sistema de rastreamento de eventos, como o Adobe Analytics. O manipulador de retorno de chamada aceita os seguintes argumentos:

   * `objID {String}` não usado no momento.
   * `compClass {String}` não usado no momento.
   * `instName {String}` um nome de instância do componente do SDK do visualizador que acionou o evento.
   * `timeStamp {Number}` carimbo de data e hora do evento.
   * `eventInfo {String}` carga do evento.

Consulte também [MixedMediaViewer](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-mixedmediaviewer.md#reference-59b70dd7b58c43059bd85e3295441195) e [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-sethandlers.md#reference-09523cf4f448400b83f7906688368bf3).
