---
title: Namespace do visualizador do SDK
description: Namespace do visualizador do SDK
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 6cbf7eef-0d17-4411-9a74-22455009f66d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# Namespace do visualizador do SDK{#viewer-sdk-namespace}

O visualizador é construído a partir de muitos componentes do SDK do visualizador. Normalmente, a página da Web não precisa interagir diretamente com a API de componentes do SDK; todas as necessidades comuns são cobertas na própria API do visualizador.

No entanto, alguns casos de uso avançados exigem que a página da Web faça referência a um componente interno do SDK usando a API do visualizador `getComponent()` e, em seguida, use toda a flexibilidade das APIs do próprio SDK.

O namespace usado para carregar e inicializar componentes do SDK pelo visualizador depende do ambiente em que o visualizador está operando. Se o visualizador estiver em execução no Adobe Experience Manager, ele carregará os componentes do SDK no namespace `s7viewers.s7sdk`. Da mesma forma, o visualizador veiculado no Dynamic Media Classic carrega a SDK em `s7classic.s7sdk`.

Em ambos os casos, o namespace usado pelo SDK dentro do visualizador tem `s7viewers` ou `s7classic` como prefixo. É diferente do namespace `s7sdk` comum usado no Guia do Usuário do SDK ou na documentação da API do SDK. Por esse motivo, é importante usar um namespace do SDK totalmente qualificado ao gravar o código de aplicativo personalizado que se comunica com componentes internos do visualizador.

Por exemplo, se você planeja ouvir o evento `StatusEvent.NOTF_VIEW_READY` e o visualizador é fornecido pela Experience Manager, o tipo de evento totalmente qualificado é `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`, e o código do ouvinte do evento é semelhante ao seguinte:

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var smartCropVideoPlayer = <instance>.getComponent("smartCropVideoPlayer"); 
   smartCropVideoPlayer.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for the viewer served from Dynamic Media Classic looks like the following: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var smartCropVideoPlayer = <instance>.getComponent("smartCropVideoPlayer"); 
   smartCropVideoPlayer.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
