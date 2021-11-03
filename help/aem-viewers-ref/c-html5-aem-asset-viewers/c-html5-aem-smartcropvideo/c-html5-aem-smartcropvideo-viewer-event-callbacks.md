---
description: Retornos de chamada do evento
solution: Experience Manager
title: Retornos de chamada do evento
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 2493208b-9030-49fa-b1fd-2f2bd524bce6
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '165'
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

Consulte também [SmartCropVideoViewer]
(../../c-html5-s7-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-smartcropvideo-viewer-javascriptapiref/r-html5-smartcropvideo-viewer-javascriptapiref-smartcropvideoviewer.md#reference-bfad5aa071c74a66a23c39a9b48dedb0) e [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-smartcropvideo-viewer-javascriptapiref/r-html5-smartcropvideo-viewer-javascriptapiref-smartcropvideoviewer.md#reference-22b373b37e8943a7be5c4d4cc21ed926).
