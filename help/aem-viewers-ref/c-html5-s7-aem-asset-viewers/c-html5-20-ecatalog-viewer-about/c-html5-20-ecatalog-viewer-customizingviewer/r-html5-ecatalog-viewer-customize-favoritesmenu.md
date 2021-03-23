---
description: A lista suspensa do menu Favoritos aparece na barra de controle. Consiste em um botão e um painel que é expandido quando um usuário clica ou toca em um botão. O painel contém ferramentas Favoritos individuais.
seo-description: A lista suspensa do menu Favoritos aparece na barra de controle. Consiste em um botão e um painel que é expandido quando um usuário clica ou toca em um botão. O painel contém ferramentas Favoritos individuais.
seo-title: Menu Favoritos
solution: Experience Manager
title: Menu Favoritos
uuid: 816e614d-8253-49a8-b57e-0b57b44db535
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo eletrônico
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 0%

---


# Menu Favoritos{#favorites-menu}

A lista suspensa do menu Favoritos aparece na barra de controle. Consiste em um botão e um painel que é expandido quando um usuário clica ou toca em um botão. O painel contém ferramentas Favoritos individuais.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A posição e o tamanho do menu Favoritos na interface do usuário do visualizador são controlados com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7favoritesmenu
```

**Propriedades CSS do botão de menu Favoritos**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem superior  </span> </p> </td> 
   <td colname="col2"> <p> O deslocamento da parte superior da barra de controle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem esquerda  </span> </p> </td> 
   <td colname="col2"> <p> A distância até ao botão seguinte à esquerda ou à esquerda da barra de controle, se este for o primeiro botão de uma linha. </p> </td> 
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

Exemplo - configure um menu Favoritos que é posicionado em quatro pixels da parte superior da barra de controle e em dez pixels do botão mais próximo à esquerda e dimensionado em 28 x 28 pixels.

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
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo  </span> </p> </td> 
   <td colname="col2"> <p> A imagem exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esse botão suporta o seletor de atributos `state`, que pode ser usado para aplicar skins diferentes a estados de botão diferentes.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - configure um botão de menu Favoritos que exibe uma imagem diferente para cada um dos quatro estados de botão diferentes.

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

A aparência do painel que contém ícones Favoritos individuais é controlada pelo seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesmenupanel
```

**Propriedades de CSS do painel de menus Favoritos**

<table id="table_B57B44C561E94F86BB1B0EC1671F26DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p>A cor de plano de fundo do painel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - configure um painel para ter uma cor transparente.

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesmenupanel { 
 background-color: transparent; 
}
```

