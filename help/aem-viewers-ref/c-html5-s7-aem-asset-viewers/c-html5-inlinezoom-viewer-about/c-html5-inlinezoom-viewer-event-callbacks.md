---
title: Retornos de chamada de evento
description: Retornos de chamada de evento
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: c54c54ae-f98f-4cd4-8c36-c7e2a9f3c6df
TQID: 'https://experienceleague.adobe.com/oz04eATq5k1G0cibZjJKvU1pA-UJXPHD5WITV-UB1n4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
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

Consulte também [FlyoutViewer](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-flyoutviewer.md#reference-b99bb25606444f46b27529ff3e960b1e) e [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-sethandlers.md#reference-74e9acb1cd0047d5bd60eea5fa5c8692).
