---
description: As miniaturas consistem em uma grade de imagens em miniatura com uma barra de rolagem opcional no lado direito para permitir a rolagem vertical.
solution: Experience Manager
title: Miniaturas
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo eletrônico
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 0%

---


# Miniaturas{#thumbnails}

As miniaturas consistem em uma grade de imagens em miniatura com uma barra de rolagem opcional no lado direito para permitir a rolagem vertical.

As miniaturas são alternadas clicando no botão de miniatura na barra de controle principal. Quando as miniaturas estão ativas, elas são exibidas no modo modal sobreposto na parte superior da interface do usuário do visualizador. A lógica do visualizador redimensiona automaticamente o contêiner de miniaturas para toda a área do visualizador.

A aparência do contêiner de miniaturas é controlada com o seguinte seletor de classe CSS:

`.s7ecatalogviewer .s7thumbnailgridview`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> O deslocamento vertical do contêiner de miniaturas na parte superior do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem superior  </span> </p> </td> 
   <td colname="col2"> <p>A margem superior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem esquerda  </span> </p> </td> 
   <td colname="col2"> <p>A margem esquerda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem direita  </span> </p> </td> 
   <td colname="col2"> <p>A margem direita. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-bottom  </span> </p> </td> 
   <td colname="col2"> <p>A margem inferior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p>A cor de fundo da área de miniaturas. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar miniaturas para ter 32 pixels de deslocamento da parte superior, 5 pixels de margem à esquerda e à direita e 8 pixels de margem na parte inferior, com `0xDDDDDD` plano de fundo.

```
.s7ecatalogviewer .s7thumbnailgridview { 
 top: 32px; 
 margin-left: 5px; 
 margin-right: 5px; 
 margin-bottom: 8px; 
 background-color: rgb(221, 221, 221); 
}
```

O espaçamento entre miniaturas é controlado com o seguinte seletor de classe CSS:

`.s7ecatalogviewer .s7thumbnailgridview .s7thumbcell`

<table id="table_1D93AB60E57F49A8838EA825CD6B7897"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem  </span> </p> </td> 
   <td colname="col2"> <p> O tamanho da margem horizontal e vertical ao redor de cada miniatura. O espaçamento horizontal real da miniatura é igual à soma da margem esquerda e direita definida para <span class="codeph"> .s7thumbcell </span>. Espaçamento entre miniaturas verticais é igual à soma das margens superior e inferior. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para definir um espaço de 10 pixels vertical e horizontalmente.

```
.s7ecatalogviewer .s7thumbnailgridview .s7thumbcell { 
 margin: 5px; 
}
```

A aparência da miniatura individual é controlada com o seguinte seletor de classe CSS:

`.s7ecatalogviewer .s7thumbnailgridview .s7thumb`

<table id="table_1D973EA6C36947F092AAA16CFE9B44A1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>A largura da miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>A altura da miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>A borda da miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p>A cor de fundo da miniatura. </p> </td> 
  </tr> 
 </tbody> 
</table>

Em dispositivos de toque, quando girado para o modo retrato, o visualizador pode dimensionar miniaturas para metade do que está configurado caso decida dividir o catálogo espalhado em páginas individuais.

>[!NOTE]
>
>A miniatura é compatível com o seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de miniatura diferentes. Especificamente, `state="selected"` corresponde à miniatura da imagem exibida no momento na exibição principal, `state="default"` corresponde ao restante das miniaturas e `state="over"` é usado ao passar o mouse.

Exemplo - para configurar miniaturas com 120 x 85 pixels, tenham um plano de fundo branco, uma borda padrão cinza-claro e uma borda selecionada cinza-escura.

```
.s7ecatalogviewer .s7thumbnailgridview .s7thumb { 
 width:120px; 
 height:85px; 
 background-color: rgb(255, 255, 255); 
 border: solid 1px #999999; 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7thumb[state="selected"]{ 
 border: solid 2px #666666; 
}
```

A aparência do rótulo de miniatura é controlada com o seguinte seletor de classe CSS:

`.s7ecatalogviewer .s7thumbnailgridview .s7label`

<table id="table_E242176042F247F8B51A0D5ADB645E20"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes  </span> </p> </td> 
   <td colname="col2"> <p>Nome da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte  </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar rótulos para usar a fonte Helvetica de 14 pixels.

```
.s7ecatalogviewer .s7thumbnailgridview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 12px; 
}
```

Caso haja mais miniaturas do que as que podem caber verticalmente na exibição, as miniaturas renderizam a barra de rolagem vertical no lado direito. A aparência da área da barra de rolagem é controlada com o seguinte seletor de classe CSS:

`.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar`

<table id="table_F05EC87CD9A946DB9B4B2B48E0784168"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>A largura da barra de rolagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> O deslocamento da barra de rolagem vertical a partir da parte superior da área de miniaturas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>O deslocamento da barra de rolagem vertical a partir da parte inferior da área de miniaturas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p> O deslocamento da barra de rolagem horizontal da borda direita da área de miniaturas. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar uma barra de rolagem com 28 pixels de largura e uma margem de 8 pixels da parte superior, direita e inferior da área de miniaturas.

```
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar { 
 top:8px; 
 bottom:8px; 
 right:8px; 
 width:28px; 
}
```

O rastreamento da barra de rolagem é a área entre os botões de rolagem superior e inferior. O componente define automaticamente a posição e a altura da faixa. A faixa é controlada com o seguinte seletor de classe CSS:

`.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrolltrack`

<table id="table_EF1B91F9E984451EB0AB48175D917726"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>A largura do rastreamento da barra de rolagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p> A cor de fundo do rastreamento da barra de rolagem. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar um rastreamento de barra de rolagem com 28 pixels de largura e um plano de fundo cinza semitransparente.

```
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrolltrack { 
 width:28px; 
 background-color:rgba(102, 102, 102, 0.5); 
}
```

O polegar da barra de rolagem se move verticalmente na área de trilha de rolagem. Sua posição vertical é totalmente controlada pela lógica do componente. No entanto, a altura da miniatura não muda dinamicamente, dependendo da quantidade de conteúdo. A altura do polegar e outros aspectos são controlados com o seguinte seletor de classe CSS:

`.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb`

<table id="table_5C791F6E90E64E7A9F1DB7C9B2FDC528"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>A largura do polegar da barra de rolagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>A altura da miniatura da barra de rolagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte superior do preenchimento  </span> </p> </td> 
   <td colname="col2"> <p>O preenchimento vertical entre a parte superior da faixa da barra de rolagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte inferior do preenchimento  </span> </p> </td> 
   <td colname="col2"> <p>O preenchimento vertical entre a parte inferior da faixa da barra de rolagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo  </span> </p> </td> 
   <td colname="col2"> <p>A imagem exibida para um determinado estado de polegar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>O botão suporta o seletor de atributos `state`, que pode ser usado para aplicar diferentes capas aos estados de polegar `up`, `down`, `over` e `disabled`.

Exemplo - para configurar um polegar da barra de rolagem que seja 28 x 45 pixels, tenha margens de 10 pixels na parte superior e inferior e tenha arte-final diferente para cada estado.

```
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb { 
 width:28px; 
 background-repeat:no-repeat; 
 background-position:center; 
 height:45px; 
 padding-top:10px; 
 padding-bottom:10px; 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_down.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_over.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
}
```

A aparência dos botões de rolagem superior e inferior é controlada pelos seguintes seletores de classe CSS:

`.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton`

`.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton`

Não é possível posicionar os botões de rolagem usando as propriedades CSS `top`, `left`, `bottom` e `right`. Em vez disso, a lógica do visualizador os posiciona automaticamente.

<table id="table_89E64A138ABF463F9650BB454F22D530"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>A largura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>A altura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo  </span> </p> </td> 
   <td colname="col2"> <p>A imagem exibida para um determinado estado de polegar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esses botões oferecem suporte ao seletor de atributos `state`, que pode ser usado para aplicar skins diferentes aos estados de botões diferentes `up`, `down`, `over` e `disabled`.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - para configurar botões de rolagem que são 28 x 32 pixels e têm arte-final diferente para cada estado.

```
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_over.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_down.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_over.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_down.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
}
```

