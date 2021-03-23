---
description: Retornos de chamada do evento
solution: Experience Manager
title: Retornos de chamada do evento
uuid: 512f5c08-cf6a-4721-a169-11977cd4c248
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de rotação
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---


# Retornos de chamada do evento{#event-callbacks}

O visualizador suporta retornos de chamada de evento JavaScript que a página da Web usa para rastrear o processo de inicialização do visualizador ou o comportamento do tempo de execução.

Os manipuladores de retorno de chamada são atribuídos transmitindo nomes de evento e funções de manipulador correspondentes com a propriedade `handlers` para `config` objeto JSON no construtor do visualizador. Como alternativa, é possível usar o método da API `setHandlers()`.

Os eventos compatíveis do visualizador incluem:

* `initComplete` - dispara quando a inicialização do visualizador é concluída e todos os componentes internos são criados, para que seja possível usar a  `getComponent()` API. O manipulador de retorno de chamada não aceita argumentos.

* `trackEvent` - dispara sempre que um evento ocorre no visualizador, o que pode ser manipulado por um sistema de rastreamento de eventos, como o Adobe Analytics. O manipulador de retorno de chamada aceita os seguintes argumentos:

   * `objID {String}` não usado no momento.
   * `compClass {String}` não usado no momento.
   * `instName {String}` um nome de instância do componente do SDK do visualizador que acionou o evento.
   * `timeStamp {Number}` carimbo de data e hora do evento.
   * `eventInfo {String}` carga do evento.

Consulte também [SpinViewer](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-spinviewer.md#reference-59b70dd7b58c43059bd85e3295441195) e [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-sethandlers.md#reference-d2223794fb45440094e9fdb5e9b73bef).
