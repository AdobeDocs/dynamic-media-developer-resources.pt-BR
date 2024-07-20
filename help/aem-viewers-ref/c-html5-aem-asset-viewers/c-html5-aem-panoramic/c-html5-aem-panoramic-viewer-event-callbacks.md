---
title: Retornos de chamada de evento
description: Retornos de chamada de evento
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 24ea35c0-a0b1-4768-9336-94eb5e2d4fb2
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '143'
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
   * `instName {String}` um nome de instância do componente do SDK do Visualizador do HTML5 que acionou o evento.
   * Carimbo de data/hora do evento `timeStamp {Number}`.
   * `eventInfo {String}` carga do evento.

