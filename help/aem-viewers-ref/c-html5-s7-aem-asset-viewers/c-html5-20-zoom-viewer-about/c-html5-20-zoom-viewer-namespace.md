---
title: Namespace do SDK do visualizador
description: Namespace do SDK do visualizador
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ad68dd09-d8df-4fc8-952a-ef82d9662de9
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# Namespace do SDK do visualizador{#viewer-sdk-namespace}

O visualizador é criado de vários componentes do SDK do visualizador. Geralmente, a página da Web não precisa interagir diretamente com a API de componentes do SDK; todas as necessidades comuns são abordadas na própria API do visualizador.

No entanto, alguns casos de uso avançado exigem que a página da Web faça referência a um componente interno do SDK usando o `getComponent()` API do visualizador e, em seguida, use toda a flexibilidade das APIs do próprio SDK.

O namespace usado para carregar e inicializar componentes do SDK pelo visualizador depende do ambiente em que o visualizador está operando. Se o visualizador estiver em execução no Adobe Experience Manager, o visualizador carregará os componentes do SDK no `s7viewers.s7sdk` namespace. Da mesma forma, o visualizador servido do Dynamic Media Classic carrega o SDK no `s7classic.s7sdk`.

Em ambos os casos, o namespace usado pelo SDK dentro do visualizador tem `s7viewers` ou `s7classic` como o prefixo. E é diferente da planície `s7sdk` namespace usado no Guia do usuário do SDK ou na documentação da API do SDK. Por esse motivo, é importante usar um namespace de SDK totalmente qualificado ao gravar um código de aplicativo personalizado que se comunique com componentes do visualizador interno.

Por exemplo, se você planeja ouvir `StatusEvent.NOTF_VIEW_READY` e o visualizador é veiculado a partir do Experience Manager, o tipo de evento totalmente qualificado é `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`e o código do ouvinte do evento é semelhante ao seguinte:

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for viewer served from Dynamic Media Classic will look like this: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
