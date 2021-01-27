---
description: Retornos de chamada de evento
solution: Experience Manager
title: Retornos de chamada de evento
topic: Dynamic Media
uuid: b9252d4b-cff1-42eb-9e56-553091f854b5
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '210'
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

* `quickViewActivate` - dispara quando um usuário clica ou toca em uma amostra interativa dentro do componente de amostras interativas ou na tela &quot;chamada para ação&quot; mostrada no final da reprodução do vídeo. O manipulador de retorno de chamada usa o único argumento que é um objeto JSON com os seguintes campos:

   * `sku` { `String`} valor SKU associado à amostra interativa.
   * `<additionalVariable>` {  `String`} zero ou mais variáveis adicionais associadas à amostra interativa.

Consulte também [InterativeVideoViewer](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-interactivevideo.md#reference-bd16cadc0c054fafb0db4994741d47cd) e [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
