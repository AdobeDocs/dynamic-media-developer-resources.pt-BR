---
description: A posição do botão é totalmente gerenciada pelo menu Favoritos.
seo-description: A posição do botão é totalmente gerenciada pelo menu Favoritos.
seo-title: Botão visualização de todos os favoritos
solution: Experience Manager
title: Botão visualização de todos os favoritos
topic: Dynamic Media
uuid: f9fd2110-d225-4eba-8e21-acc9c0e1dfd4
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# Botão visualização de todos os favoritos{#view-all-favorites-button}

A posição do botão é totalmente gerenciada pelo menu Favoritos.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A aparência do botão Visualização Todos os favoritos é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7viewallfavoritebutton
```

**Propriedades de CSS do botão Remover favorito**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> A imagem que é exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da sprite de arte, se os sprites CSS forem usados. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão suporta os seletores de atributos `state` e `selected`, que podem ser usados para aplicar diferentes capas a diferentes estados de botão. Em particular, `selected='true'` corresponde ao estado em que um usuário pode adicionar um novo ícone Favorito clicando ou tocando. `selected='false'` corresponde ao modo de operação normal quando um usuário pode aplicar zoom, deslocar e trocar páginas.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização de elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - para configurar um botão Visualização Todos os favoritos com 28 x 28 pixels e exibe uma imagem diferente para cada um dos quatro estados de botão diferentes quando selecionado ou não selecionado.

```
.s7ecatalogviewer .s7viewallfavoritebutton { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='false'][state='up'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_up.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='false'][state='over'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_over.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='false'][state='down'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_down.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='false'][state='disabled'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_disabled.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='true'][state='up'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_over.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='true'][state='over'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_over.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='true'][state='down'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_over.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='true'][state='disabled'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_disabled.png); 
}
```

