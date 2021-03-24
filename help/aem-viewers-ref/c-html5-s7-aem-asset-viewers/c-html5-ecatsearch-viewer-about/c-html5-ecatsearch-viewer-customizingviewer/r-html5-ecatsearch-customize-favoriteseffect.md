---
description: O visualizador exibe ícones Favoritos sobre a exibição principal nos locais em que ele foi adicionado originalmente pelo usuário.
solution: Experience Manager
title: Efeito Favoritos
feature: Dynamic Media Classic,Visualizadores,SDK/API,Pesquisa de catálogo eletrônico
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---


# Efeito Favoritos{#favorites-effect}

O visualizador exibe ícones Favoritos sobre a exibição principal nos locais em que ele foi adicionado originalmente pelo usuário.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A aparência do ícone Favorito é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7favoriteseffect .s7icon
```

**Propriedades CSS do ícone Favorito**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo  </span> </p> </td> 
   <td colname="col2"> <p> A imagem exibida para o ícone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largura do ícone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do ícone. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - configure um ícone de 36 x 36 pixels Favoritos.

```
.s7ecatalogsearchviewer .s7favoriteseffect .s7icon { 
 height: 36px; 
 width: 36px;  
 background-image: url(images/v2/FavoriteEffect_dark_up.png); 
}
```

Em sistemas de desktop, o componente suporta o seletor de atributos `cursortype` que você pode aplicar à classe `.s7favoriteseffect` e controla o tipo do cursor com base na ação do usuário selecionado. Os seguintes valores `cursortype` são suportados:

<table id="table_71F8F333909247E4ACFEBDE3A1370EAB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_add  </span> </p> </td> 
   <td colname="col2"> <p>O usuário exibido está adicionando um novo ícone Favorito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_remove  </span> </p> </td> 
   <td colname="col2"> <p>O usuário exibido está removendo um ícone Favorito existente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_view  </span> </p> </td> 
   <td colname="col2"> <p>Exibido no modo de operação normal quando a edição de Favoritos não está ativa. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - tem cursores de mouse diferentes para cada tipo de estado de componente.

```
.s7ecatalogsearchviewer .s7favoriteseffect[cursortype="mode_add"] { 
cursor: crosshair; 
} 
.s7ecatalogsearchviewer .s7favoriteseffect[cursortype="mode_remove"] { 
cursor: not-allowed; 
} 
.s7ecatalogsearchviewer .s7favoriteseffect[cursortype="mode_view"] { 
cursor: auto; 
}
```

