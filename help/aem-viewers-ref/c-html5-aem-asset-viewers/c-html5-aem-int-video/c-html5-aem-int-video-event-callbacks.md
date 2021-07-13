---
description: Retornos de chamada do evento
solution: Experience Manager
title: Retornos de chamada do evento
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interativos
role: Developer,User
exl-id: af051437-28e5-416f-a61a-0abafb1814b2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '218'
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

* `quickViewActivate` - dispara quando um usuário clica ou toca em uma amostra interativa no componente de amostras interativas ou na tela &quot;chamar a ação&quot; mostrada no final da reprodução do vídeo. O manipulador de retorno de chamada pega o único argumento que é um objeto JSON com os seguintes campos:

   * `sku` Valor do SKU { `String`} associado à amostra interativa.
   * `<additionalVariable>` {  `String`} zero ou mais variáveis adicionais associadas à amostra interativa.

Consulte também [InterativeVideoViewer](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-interactivevideo.md#reference-bd16cadc0c054fafb0db4994741d47cd) e [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
