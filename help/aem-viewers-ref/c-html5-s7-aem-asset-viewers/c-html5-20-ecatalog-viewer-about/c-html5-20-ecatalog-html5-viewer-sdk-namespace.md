---
title: Namespace do SDK do visualizador
description: Namespace do SDK do visualizador
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: c5286e1f-1f43-4cb8-b876-dc843f8112f5
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# Namespace do SDK do visualizador{#viewer-sdk-namespace}

O visualizador é criado de vários componentes do SDK do visualizador. Geralmente, a página da Web não precisa interagir diretamente com a API de componentes do SDK; todas as necessidades comuns são abordadas na própria API do visualizador.

No entanto, alguns casos de uso avançado exigem que a página da Web faça referência a um componente interno do SDK usando o `getComponent()` API do visualizador e, em seguida, use toda a flexibilidade das APIs do próprio SDK.

O namespace usado para carregar e inicializar componentes do SDK pelo visualizador depende do ambiente em que o visualizador está operando. Se o visualizador estiver em execução no Adobe Experience Manager, o visualizador carregará os componentes do SDK no `s7viewers.s7sdk` namespace. E o visualizador veiculado pelo Dynamic Media Classic carrega o SDK no `s7classic.s7sdk`.

Em ambos os casos, o namespace usado pelo SDK dentro do visualizador tem `s7viewers` ou `s7classic` como o prefixo. E é diferente da planície `s7sdk` namespace usado no Guia do usuário do SDK ou na documentação da API do SDK.

Por esse motivo, é importante usar um namespace de SDK totalmente qualificado ao gravar um código de aplicativo personalizado que se comunique com componentes do visualizador interno.

Por exemplo, se você planeja ouvir `StatusEvent.NOTF_VIEW_READY` e o visualizador é veiculado no Dynamic Media Classic, o tipo de evento totalmente qualificado é `s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY`e o código do ouvinte do evento é semelhante ao seguinte:

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var pageView = <instance>.getComponent("pageView"); 
   pageView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
