---
description: Namespace do SDK do visualizador
solution: Experience Manager
title: Namespace do SDK do visualizador
feature: Dynamic Media Classic,Visualizadores,SDK/API,Banners em carrossel
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---


# Namespace do SDK do visualizador{#viewer-sdk-namespace}

O visualizador é criado de vários componentes do SDK do visualizador. Na maioria dos casos, a página da Web não precisa interagir diretamente com a API de componentes do SDK; todas as necessidades comuns são abordadas na própria API do visualizador.

No entanto, alguns casos de uso avançados exigem que a página da Web obtenha uma referência a um componente interno do SDK usando a `getComponent()` API do visualizador e, em seguida, use toda a flexibilidade das APIs do próprio SDK.

O namespace usado para carregar e inicializar componentes do SDK pelo visualizador depende do ambiente em que o visualizador está operando. Se o visualizador estiver em execução no AEM (Adobe Experience Manager), o visualizador carregará os componentes do SDK no namespace `s7viewers.s7sdk`. E o visualizador veiculado pelo Dynamic Media Classic carrega o SDK em `s7classic.s7sdk`.

Em ambos os casos, o namespace usado pelo SDK dentro do visualizador tem `s7viewers` ou `s7classic` como o prefixo. E é diferente do namespace simples `s7sdk` usado no Guia do usuário do SDK ou na documentação da API do SDK.

Por esse motivo, é importante usar um namespace de SDK totalmente qualificado ao gravar um código de aplicativo personalizado que se comunique com componentes do visualizador interno.

Por exemplo, se você planeja ouvir o evento `StatusEvent.NOTF_VIEW_READY` e o visualizador for exibido a partir de AEM, o tipo de evento totalmente qualificado é `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`, e o código do ouvinte do evento é semelhante ao seguinte:

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var carouselView = <instance>.getComponent("carouselView"); 
   carouselView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```

