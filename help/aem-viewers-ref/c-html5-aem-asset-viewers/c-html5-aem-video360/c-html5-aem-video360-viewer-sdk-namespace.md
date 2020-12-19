---
description: nulo
seo-description: nulo
seo-title: Namespace do SDK do visualizador
solution: Experience Manager
title: Namespace do SDK do visualizador
topic: Dynamic media
uuid: e0113556-708c-4898-93f9-b3888de00afc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---


# Namespace do SDK do visualizador{#viewer-sdk-namespace}

O visualizador foi criado com vários componentes do SDK do visualizador. Na maioria dos casos, a página da Web não precisa interagir diretamente com a API de componentes do SDK; todas as necessidades comuns são abordadas na própria API do visualizador.

No entanto, alguns casos de uso avançado exigem que a página da Web obtenha uma referência a um componente SDK interno usando a `getComponent()` API do visualizador e use toda a flexibilidade das APIs do próprio SDK.

A namespace usada para carregar e inicializar componentes do SDK pelo visualizador depende do ambiente no qual o visualizador está operando. Se o visualizador estiver sendo executado no AEM (Adobe Experience Manager), o visualizador carregará os componentes do SDK na namespace `s7viewers.s7sdk`. Da mesma forma, o visualizador fornecido pelo Scene7 Publishing System carrega o SDK em `s7classic.s7sdk`.

Em ambos os casos, a namespace usada pelo SDK dentro do visualizador tem `s7viewers` ou `s7classic` como o prefixo. Além disso, é diferente da namespace simples `s7sdk` usada no Guia do usuário do SDK ou na documentação da API do SDK.

Por esse motivo, é importante usar uma namespace SDK totalmente qualificada ao gravar um código de aplicativo personalizado que se comunica com componentes do visualizador interno.

Por exemplo, se você planeja ouvir o evento `StatusEvent.NOTF_VIEW_READY` e o visualizador for servido a partir do AEM, o tipo de evento totalmente qualificado será `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` e o código do ouvinte do evento será semelhante ao seguinte:

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var videoPlayer = <instance>.getComponent("videoPlayer"); 
   videoPlayer.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```

