---
description: O visualizador exibe os ícones Favoritos sobre a visualização principal nos locais em que ele foi adicionado originalmente pelo usuário.
seo-description: O visualizador exibe os ícones Favoritos sobre a visualização principal nos locais em que ele foi adicionado originalmente pelo usuário.
seo-title: Efeito Favoritos
solution: Experience Manager
title: Efeito Favoritos
topic: Dynamic Media
uuid: b660b9fd-592b-4072-83c9-f70330ee19ab
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---


# Efeito Favoritos{#favorites-effect}

O visualizador exibe os ícones Favoritos sobre a visualização principal nos locais em que ele foi adicionado originalmente pelo usuário.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A aparência do ícone Favorito é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7favoriteseffect .s7icon
```

**Propriedades de CSS do ícone Favorito**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> A imagem exibida para o ícone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da sprite de arte, se os sprites CSS forem usados. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
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
.s7ecatalogviewer .s7favoriteseffect .s7icon { 
 height: 36px; 
 width: 36px;  
 background-image: url(images/v2/FavoriteEffect_dark_up.png); 
}
```

Em sistemas de desktop, o componente suporta o seletor de atributos `cursortype` que você pode aplicar à classe `.s7favoriteseffect` e controla o tipo de cursor com base na ação do usuário selecionada. Os seguintes valores `cursortype` são suportados:

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
   <td colname="col1"> <p> <span class="codeph"> mode_visualização  </span> </p> </td> 
   <td colname="col2"> <p>Exibida no modo de operação normal quando a edição de Favoritos não está ativa. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - tem cursores de mouse diferentes para cada tipo de estado do componente.

```
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_add"] { 
cursor: crosshair; 
} 
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_remove"] { 
cursor: not-allowed; 
} 
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_view"] { 
cursor: auto; 
}
```

