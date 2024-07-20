---
title: Menu Favoritos
description: A lista suspensa do menu Favoritos é exibida na barra de controle. Consiste em um botão e um painel que se expande quando um usuário clica ou toca em um botão. O painel contém ferramentas Favoritos individuais.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e3c90320-b6fc-4a43-b75f-d39234b1e73c
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---

# Menu Favoritos{#favorites-menu}

A lista suspensa do menu Favoritos é exibida na barra de controle. Consiste em um botão e um painel que se expande quando um usuário clica ou toca em um botão. O painel contém ferramentas Favoritos individuais.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A posição e o tamanho do menu Favoritos na interface do usuário do visualizador são controlados com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7favoritesmenu
```

**Propriedades CSS do botão do menu Favoritos**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem superior </span> </p> </td> 
   <td colname="col2"> <p> O deslocamento da parte superior da barra de controle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem esquerda </span> </p> </td> 
   <td colname="col2"> <p> A distância até o próximo botão à esquerda ou à esquerda da barra de controle, se este for o primeiro botão consecutivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - Para configurar um menu Favoritos posicionado a quatro pixels da parte superior da barra de controle e a dez pixels do botão mais próximo à esquerda e dimensionado a 28 x 28 pixels:

```
.s7ecatalogviewer .s7favoritesmenu { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
}
```

A aparência do botão de menu Favoritos é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton
```

**Propriedades CSS do botão Favoritos**

<table id="table_970D62A1413145E0A964FA9D9F108579"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo </span> </p> </td> 
   <td colname="col2"> <p> A imagem exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão oferece suporte ao seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - Para configurar um botão do menu Favoritos que exibe uma imagem diferente para cada um dos quatro estados de botão diferentes:

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='up'] { 
background-image:url(images/v2/FavoritesMenu dark_up.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='over'] { 
background-image:url(images/v2/FavoritesMenu_dark_over.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='down'] { 
background-image:url(images/v2/FavoritesMenu_dark_down.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='disabled'] { 
background-image:url(images/v2/FavoritesMenu_dark_disabled.png); 
}
```

A aparência do painel que contém ícones Favoritos individuais é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesmenupanel
```

**Propriedades CSS do painel de menu Favoritos**

<table id="table_B57B44C561E94F86BB1B0EC1671F26DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p>A cor do plano de fundo do painel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - Para configurar um painel com uma cor transparente:

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesmenupanel { 
 background-color: transparent; 
}
```
