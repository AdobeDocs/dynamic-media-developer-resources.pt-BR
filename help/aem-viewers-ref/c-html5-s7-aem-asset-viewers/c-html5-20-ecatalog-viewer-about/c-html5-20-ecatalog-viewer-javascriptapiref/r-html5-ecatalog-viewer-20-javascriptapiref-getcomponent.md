---
description: Referência da API JavaScript para o eCatalog Viewer
seo-description: Referência da API JavaScript para o eCatalog Viewer
seo-title: getComponent
solution: Experience Manager
title: getComponent
topic: Dynamic media
uuid: e06e2943-d2cc-4eaf-9fd4-4225bb7a7469
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---


# getComponent{#getcomponent}

Referência da API JavaScript para o eCatalog Viewer

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
   <td colname="col1"> <p> <span class="codeph"> pageView  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.PageView  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PrimaryControls  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ControlBar  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> secondaryControls  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ControlBar  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gridView  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.ThumbnailGridView  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tableOfContents  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.TableOfContents  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> infoPanelPopup  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.info.InfoPanelPopup  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imageMapEffect  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.ImageMapEffect  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> leftButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanLeftButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rightButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanRightButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomInButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomInButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomOutButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomOutButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomResetButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomResetButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> secondaryZoomResetButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomResetButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> thumbnailPageButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ThumbnailPageButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fullScreenButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.FullScreenButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> toolBarLeftButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanLeftButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> toolBarRightButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanRightButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> firstPageButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanLeftButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> secondaryFirstPageButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanLeftButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> lastPageButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanRightButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> secondaryLastPageButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanRightButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> closeButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.CloseButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> socialShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.SocialShare  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> twitterShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.TwitterShare  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> facebookShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.FacebookShare  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> linkShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.LinkShare  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> emailShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.EmailShare  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> embedShare  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.EmbedShare  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> print  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.Print  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> download  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Download  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> favoritesEffect  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.favorites.FavoritesEffect  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> favoritesView  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.favorites.FavoritesView  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> favoritesMenu  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.favorites.FavoritesMenu  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> addFavoriteButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.favorites.AddFavoriteButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> removeFavoriteButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.favorites.RemoveFavoriteButton  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> viewAllFavoriteButton  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.favorites.ViewAllFavoriteButton  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Ao trabalhar com as APIs do SDK, é importante usar a namespace correta do SDK totalmente qualificado, conforme descrito em [namespace do SDK do visualizador](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-html5-viewer-sdk-namespace.md#concept-16ce67bfbdc64ffc8fc7ad174f208f05).

Consulte a documentação *API do SDK do visualizador* para obter mais informações sobre um componente específico.

## Retorna {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` uma referência ao componente SDK do visualizador. O método retornará `null` se `componentId` não for um componente do visualizador suportado ou se o componente ainda não tiver sido criado pela lógica do visualizador.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var pageView = <instance>.getComponent("pageView"); 
} 
})
```

