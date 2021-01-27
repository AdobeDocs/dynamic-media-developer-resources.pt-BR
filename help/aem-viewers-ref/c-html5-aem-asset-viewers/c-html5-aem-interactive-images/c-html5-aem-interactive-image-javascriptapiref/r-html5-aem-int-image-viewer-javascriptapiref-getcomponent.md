---
description: Referência da API JavaScript para o Visualizador de imagens de vídeo.
seo-description: Referência da API JavaScript para o Visualizador de imagens de vídeo.
seo-title: getComponent
solution: Experience Manager
title: getComponent
topic: Dynamic Media
uuid: 6dd112f1-7b34-4d04-969e-b0cef46b4ad4
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---


# getComponent{#getcomponent}

Referência da API JavaScript para o Visualizador de imagens de vídeo.

`getComponent(componentId)`

Retorna uma referência ao componente do SDK do visualizador que é usado pelo visualizador. A página da Web pode usar esse método para estender ou personalizar o comportamento do visualizador predefinido. Chame esse método somente depois que a chamada de retorno do visualizador `initComplete` for executada, caso contrário, o componente ainda não poderá ser criado pela lógica do visualizador.

## Parâmetros {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*`  -  `{String}` uma ID do componente SDK do visualizador usado pelo visualizador. Este visualizador suporta as seguintes IDs de componente:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ID do componente </p> </th> 
   <th colname="col2" class="entry"> <p>Nome da classe do componente SDK do visualizador </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> container  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomView  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.ZoomView  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imageMapEffect  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.mageMapEffect  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Ao trabalhar com APIs do SDK, é importante usar a namespace SDK totalmente qualificada correta, conforme descrito em [namespace do SDK do visualizador](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-namespace.md#concept-00a31b9bc7eb4014b28c1ba661fe5265).

Consulte a documentação da API do SDK do visualizador para obter mais informações sobre um componente específico.

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` uma referência ao componente SDK do visualizador. O método retornará `null` se `componentId` não for um componente do visualizador suportado ou se o componente ainda não tiver sido criado pela lógica do visualizador.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
} 
})
```

