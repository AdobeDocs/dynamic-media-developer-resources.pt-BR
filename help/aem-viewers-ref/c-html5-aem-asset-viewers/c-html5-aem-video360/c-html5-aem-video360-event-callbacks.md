---
title: Retornos de chamada de evento
description: Retornos de chamada de evento
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 24ea35c0-a0b1-4768-9336-94eb5e2d4fb2
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# Retornos de chamada de evento{#event-callbacks}

O visualizador suporta retornos de chamada de evento JavaScript que a página da Web usa para rastrear o processo de inicialização do visualizador ou o comportamento do tempo de execução.

Os manipuladores de retorno de chamada são atribuídos passando nomes de evento e funções de manipulador correspondentes com o `handlers` propriedade para `config` Objeto JSON no construtor do visualizador. Alternativamente, é possível utilizar `setHandlers()` método da API.

Os eventos do visualizador compatíveis incluem o seguinte:

* `initComplete` - é acionado quando a inicialização do visualizador é concluída e todos os componentes internos são criados, para que seja possível usar `getComponent()` API. O manipulador de retorno de chamada não aceita argumentos.
* `trackEvent` - é acionado sempre que um evento ocorre dentro do visualizador, que pode ser manipulado por um sistema de rastreamento de eventos, como o Adobe Analytics. O manipulador de retorno de chamada usa os seguintes argumentos:

   * `objID {String}` não usado no momento.
   * `compClass {String}` não usado no momento.
   * `instName {String}` um nome de instância do componente do SDK do Visualizador do HTML5 que acionou o evento.
   * `timeStamp {Number}` carimbo de data e hora do evento.
   * `eventInfo {String}` carga útil do evento.

Consulte também [Video360Viewer](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-video360viewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) e [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
