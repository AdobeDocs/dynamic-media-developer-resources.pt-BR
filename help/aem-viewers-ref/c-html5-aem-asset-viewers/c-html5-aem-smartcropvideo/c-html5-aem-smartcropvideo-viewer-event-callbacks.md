---
title: Retornos de chamada de evento
description: Retornos de chamada de evento
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 21962c01-f224-408d-8072-1c7f5d78ac4b
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '150'
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
   * `eventInfo {String}` carga do evento.

Consulte também [SmartCropVideoViewer]
(/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-smartcropvideoviewer.md) e [setHandlers](/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-sethandlers.md).
