---
description: As amostras consistem em uma linha de imagens em miniatura com botões de rolagem opcionais no lado esquerdo e direito. Os botões de rolagem só ficam visíveis na área de trabalho se todas as miniaturas não puderem se ajustar à largura do container. Em dispositivos móveis, ou se as miniaturas puderem se ajustar à largura do container, os botões de rolagem não serão exibidos.
seo-description: As amostras consistem em uma linha de imagens em miniatura com botões de rolagem opcionais no lado esquerdo e direito. Os botões de rolagem só ficam visíveis na área de trabalho se todas as miniaturas não puderem se ajustar à largura do container. Em dispositivos móveis, ou se as miniaturas puderem se ajustar à largura do container, os botões de rolagem não serão exibidos.
seo-title: Amostras
solution: Experience Manager
title: Amostras
topic: Dynamic media
uuid: d44e775d-5253-4990-98a4-84ff50db09b9
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Amostras{#swatches}

As amostras consistem em uma linha de imagens em miniatura com botões de rolagem opcionais no lado esquerdo e direito. Os botões de rolagem só ficam visíveis na área de trabalho se todas as miniaturas não puderem se ajustar à largura do container. Em dispositivos móveis, ou se as miniaturas puderem se ajustar à largura do container, os botões de rolagem não serão exibidos.

`.s7zoomviewer .s7swatches`

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades de CSS da área do visualizador principal**

A aparência do container de amostras é controlada com o seguinte seletor de classe CSS:

```
.s7zoomviewer .s7zoomresetbutton
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largura das amostras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura das amostras. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>As amostras verticais são deslocadas em relação ao container do visualizador. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar amostras para 460 x 100 pixels.

```
.s7zoomviewer .s7swatches { 
 width: 460px; 
 height: 100px;  
}
```

O espaçamento entre as miniaturas da amostra é controlado com o seguinte seletor de classe CSS:

`.s7zoomviewer .s7swatches .s7thumbcell`

<table id="table_565B354FEA814804A0BE3978E1242110"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem </span> </p> </td> 
   <td colname="col2"> <p> O tamanho da margem horizontal e vertical ao redor de cada miniatura. O espaçamento real das miniaturas é igual à soma das margens esquerda e direita definidas para <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemplo**

Para definir o espaçamento como dez pixels, tanto na vertical quanto na horizontal.

```
.s7zoomviewer .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

A aparência da miniatura individual é controlada pelo seguinte seletor de classe CSS:

`.s7zoomviewer .s7swatches .s7thumb`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largura da miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura da miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fronteira </span> </p> </td> 
   <td colname="col2"> <p>Borda da miniatura. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>A miniatura suporta o seletor de `state` atributos, que pode ser usado para aplicar diferentes capas a diferentes estados de miniaturas. Em particular, `state="selected"` corresponde à miniatura da imagem que está sendo exibida atualmente na visualização principal, `state="default"` corresponde ao restante das miniaturas e `state="over"` é usada ao passar o mouse.

Exemplo - para configurar miniaturas com 56 x 56 pixels, uma borda padrão cinza claro e uma borda cinza escura selecionada.

```
.s7zoomviewer .s7swatches .s7thumb { 
 width: 56px; 
 height: 56px;  
} 
.s7zoomviewer .s7swatches .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7zoomviewer .s7swatches .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

A aparência dos botões de rolagem à esquerda e à direita são controlados com os seguintes seletores de classe CSS:

`.s7zoomviewer .s7swatches .s7scrollleftbutton`

`.s7zoomviewer .s7swatches .s7scrollrightbutton`

Não é possível posicionar botões de rolagem usando as propriedades CSS superior, esquerda, inferior e direita. Em vez disso, a lógica do visualizador os posiciona automaticamente.

<table id="table_A5663C4AAC4446168CAD8DBA2894BB9C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão de rolagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão de rolagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>A imagem que é exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da sprite de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#section-0711ece44a4740168cfd7624c9010bd1" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão suporta o seletor de `state` atributos, que pode ser usado para aplicar diferentes capas a diferentes estados de botão: `up`, `down`, `over`e `disabled`.

As dicas de ferramentas do botão podem ser localizadas. Consulte [Localização de elementos](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)da interface do usuário.

Exemplo - para configurar botões de rolagem com 56 x 56 pixels e arte-final diferente para cada estado.

```
.s7zoomviewer .s7swatches .s7scrollleftbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7zoomviewer .s7swatches .s7scrollleftbutton[state="up"]{ 
background-image:url(images/v2/ScrollLeftButton_up.png); 
} 
.s7zoomviewer .s7swatches .s7scrollleftbutton[state="over"]{ 
 background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7zoomviewer .s7swatches .s7scrollleftbutton[state="down"]{ 
 background-image:url(images/v2/ScrollLeftButton_down.png); 
} 
.s7zoomviewer .s7swatches .s7scrollleftbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollLeftButton_disabled.png); 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton[state="up"]{ 
background-image:url(images/v2/ScrollRightButton_up.png); 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton[state="over"]{ 
 background-image:url(images/v2/ScrollRightButton_over.png); 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton[state="down"]{ 
 background-image:url(images/v2/ScrollRightButton_down.png); 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollRightButton_disabled.png); 
}
```

