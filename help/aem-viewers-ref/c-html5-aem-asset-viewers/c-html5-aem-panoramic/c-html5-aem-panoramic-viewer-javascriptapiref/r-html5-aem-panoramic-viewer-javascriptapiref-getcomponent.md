---
title: getComponent
description: Referência da API do JavaScript para o Visualizador panorâmico.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 3c228b84-fbad-434f-96b4-d52485711844
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---

# getComponent{#getcomponent}

Referência da API do JavaScript para o Visualizador panorâmico

`getComponent(componentId)`


Retorna uma referência ao componente de SDK do Visualizador usado pelo visualizador. A página da Web pode usar esse método para estender ou personalizar o comportamento do visualizador pronto para uso. Chame esse método somente após a execução do retorno de chamada do visualizador `initComplete`, caso contrário, o componente pode não ser criado ainda pela lógica do visualizador.

## Parâmetros {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*` - `{String}` uma ID do componente do SDK do Visualizador usado pelo visualizador. Esse visualizador é compatível com as seguintes IDs de componente:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ID do componente </p> </th> 
   <th colname="col2" class="entry"> <p>Nome da classe do componente do visualizador do SDK </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contêiner </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> panoramicView </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.PanoramicView </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Ao trabalhar com APIs de SDK, é importante usar o namespace de SDK totalmente qualificado correto, conforme descrito em [Namespace de SDK do visualizador](../../../c-html5-aem-asset-viewers/c-html5-aem-panoramic/c-html5-aem-panoramic-viewer-sdk-namespace.md#concept-4ee8657c7d67421f8e7880130a246621).

Consulte a documentação da API do Visualizador SDK para obter mais informações sobre um componente específico.

## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` uma referência ao componente do Visualizador do SDK. O método retornará `null` se `componentId` não for um componente de visualizador com suporte ou se o componente ainda não tiver sido criado pela lógica do visualizador.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var panoramicView = <instance>.getComponent("panoramicView"); 
} 
})
```
