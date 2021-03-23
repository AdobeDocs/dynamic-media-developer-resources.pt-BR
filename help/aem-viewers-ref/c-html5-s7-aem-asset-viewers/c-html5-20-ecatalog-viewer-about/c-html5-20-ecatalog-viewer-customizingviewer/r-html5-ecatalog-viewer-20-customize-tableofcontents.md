---
description: Índice é um botão localizado na barra de controle principal. Quando ativado, um painel suspenso é exibido com uma lista de índices e rótulos de página.
seo-description: Índice é um botão localizado na barra de controle principal. Quando ativado, um painel suspenso é exibido com uma lista de índices e rótulos de página.
seo-title: Índice
solution: Experience Manager
title: Índice
uuid: e5da89b4-fd3f-41ab-bc55-d43c2999d4b7
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo eletrônico
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 0%

---


# Índice{#table-of-contents}

Índice é um botão localizado na barra de controle principal. Quando ativado, um painel suspenso é exibido com uma lista de índices e rótulos de página.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Com base na configuração, a lista pode conter todas as páginas que estão presentes no catálogo ou apenas as páginas que têm rótulos explícitos definidos. Em sistemas de desktop, se a lista for maior que o tamanho real da tela disponível, uma barra de rolagem será exibida à direita.

A posição e o tamanho do botão do índice na interface do usuário do visualizador são controlados com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7tableofcontents
```

**Propriedades CSS do índice**

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
   <td colname="col2"> <p> A largura do botão do índice. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p> A altura do botão do índice. </p> </td> 
  </tr> 
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

Exemplo - configure um botão de índice posicionado 4 pixels da parte inferior e 43 pixels da esquerda da barra de controle principal; O tamanho é 28 x 28 pixels e uma imagem diferente é exibida para cada um dos quatro estados de botão diferentes:

```
.s7ecatalogviewer .s7tableofcontents { 
margin-top: 4px; 
margin-left: 10px; width: 28px; 
 height: 28px; 
} 
.s7ecatalogviewer .s7tableofcontents[state='up'] { 
background-image:url(images/v2/TableOfContents_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='over'] { 
background-image:url(images/v2/TableOfContents_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='down'] { 
background-image:url(images/v2/TableOfContents_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='disabled'] { 
background-image:url(images/v2/TableOfContents_dark_disabled.png); 
}
```

A aparência do painel suspenso é controlada com o seguinte seletor de classe CSS:

```
 .s7ecatalogviewer .s7tableofcontents .s7panel
```

**Propriedades de CSS do painel suspenso**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p> Cor do plano de fundo do painel suspenso. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem  </span> </p> </td> 
   <td colname="col2"> <p> Deslocamento interno entre os limites do painel e o conteúdo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sombra de caixa  </span> </p> </td> 
   <td colname="col2"> <p> Sombra ao redor do painel. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Não é possível controlar o tamanho ou a posição do painel suspenso a partir do CSS; o componente gerencia seu layout de forma programática.

Exemplo - configure um painel suspenso que tenha um plano de fundo preto semitransparente, uma margem de 5 pixels em torno do conteúdo e uma sombra:

```
.s7ecatalogviewer .s7tableofcontents .s7panel { 
 background-color: rgba(0, 0, 0, 0.5); 
 margin: 5px; 
 box-shadow: 2px 2px 3px #c0c0c0; 
}
```

A aparência e comportamento individual do item é controlada com o seguinte seletor de classe CSS:

```
 .s7ecatalogviewer .s7tableofcontents .s7panel .s7item
```

**Propriedades CSS do item**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes  </span> </p> </td> 
   <td colname="col2"> <p>Nome da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte  </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do item. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento  </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>O item de lista suspensa é compatível com o seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de passar o mouse e itens selecionados.

Exemplo - configure um item suspenso com uma fonte Helvetica de 14 pixels e 19 pixels de altura. Um item tem um plano de fundo cinza escuro ao passar o mouse e um plano de fundo cinza claro quando selecionado:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item { 
font-family: Helvetica,sans-serif; 
font-size: 14px; 
height: 19px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item[state="over"] { 
background-color: rgb(102, 102, 102); 
} 
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item[state="selected"] { 
background-color: rgb(178, 178, 178); 
}
```

Um elemento que mostra o índice de página é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index
```

**Propriedades CSS do índice de página**

<table id="table_FAA5072E4AAC48F4BE00B05D87FD9827"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura mínima  </span> </p> </td> 
   <td colname="col2"> <p> Largura mínima do elemento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura máxima  </span> </p> </td> 
   <td colname="col2"> <p> Largura máxima do elemento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento à direita  </span> </p> </td> 
   <td colname="col2"> <p> Distância entre o índice de página e o rótulo da página. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>É possível ocultar o índice de página completamente definindo `display:none` para a classe CSS `s7index`.

Exemplo 1 - configure um índice de página com uma largura mínima de 40 pixels, uma largura máxima de 70 pixels e uma margem de 5 pixels no lado direito:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index { 
max-width: 70px; 
min-width: 40px; 
padding-right: 5px; 
}
```

Exemplo 2 - ocultar índice de página:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index { 
display: none; 
}
```

O rótulo da página é controlado com o seguinte seletor de classe CSS:

```
 .s7ecatalogviewer .s7tableofcontents .s7panel .s7label
```

**Propriedades CSS do rótulo da página**

<table id="table_A42E372D931D4F04855EE5AB5530CB12"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura mínima  </span> </p> </td> 
   <td colname="col2"> <p> Largura mínima do elemento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura máxima  </span> </p> </td> 
   <td colname="col2"> <p> Largura máxima do elemento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - configure um índice de página com uma largura mínima de 40 pixels e uma largura máxima de 240 pixels:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7label { 
min-width: 40px; 
max-width: 240px; 
}
```

Caso haja mais itens que possam caber verticalmente no painel suspenso e o sistema seja uma área de trabalho, o componente renderiza uma barra de rolagem vertical no lado direito do painel. A aparência da área da barra de rolagem é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar
```

**Propriedades CSS da barra de rolagem**

<table id="table_D34A63AAE6324699ABDCC08355D33035"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p> A largura da barra de rolagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> O deslocamento da barra de rolagem vertical a partir da parte superior da área do painel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p> O deslocamento da barra de rolagem vertical a partir da parte inferior da área do painel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p> O deslocamento da barra de rolagem horizontal da borda direita da área do painel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - configure uma barra de rolagem com 28 pixels de largura e não tenha uma margem para a área superior, direita ou inferior do painel:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:28px; 
}
```

O rastreamento da barra de rolagem é a área entre os botões de rolagem superior e inferior. O componente define automaticamente a posição e a altura da faixa. A faixa é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolltrack
```

**Propriedades de CSS da faixa de rolagem**

<table id="table_E49EE04B3FF64AB2948E7C09DF3EA1B7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>A largura da faixa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p>A cor do plano de fundo da faixa. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - configure um rastreamento de barra de rolagem com 28 pixels de largura e um plano de fundo cinza semitransparente:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolltrack { 
 width:28px; 
 background-color:rgba(102, 102, 102, 0.5); 
}
```

O polegar da barra de rolagem se move verticalmente na área de trilha de rolagem. Sua posição vertical é controlada pela lógica do componente. No entanto, a altura do polegar não muda dinamicamente, dependendo da quantidade de conteúdo. Você pode configurar a altura do polegar e outros aspectos com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb
```

**Propriedades CSS do polegar da barra de rolagem**

<table id="table_D8DFBC2419BD4AB3B4892AC7B599C70A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>A largura do polegar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>A altura do polegar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte superior do preenchimento  </span> </p> </td> 
   <td colname="col2"> <p> O preenchimento vertical entre a parte superior da faixa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte inferior do preenchimento  </span> </p> </td> 
   <td colname="col2"> <p>O preenchimento vertical entre a parte inferior da faixa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo  </span> </p> </td> 
   <td colname="col2"> <p> A imagem exibida para um determinado estado de polegar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>O botão suporta o seletor de atributos `state`, que pode ser usado para aplicar skins diferentes aos estados de miniatura `up`, `down`, `over` e `disabled`.

Exemplo - configure um polegar da barra de rolagem que seja 28 x 45 pixels, tenha margens de 10 pixels na parte superior e inferior e tenha uma arte-final diferente para cada estado:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb { 
 width:28px; 
 background-repeat:no-repeat; 
 background-position:center; 
 height:45px; 
 padding-top:10px; 
 padding-bottom:10px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
}
```

A aparência dos botões de rolagem superior e inferior é controlada pelos seguintes seletores de classe CSS:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton
```

Não é possível posicionar os botões de rolagem usando as propriedades CSS `top`, `left`, `bottom` e `right`; em vez disso, a lógica do visualizador os posiciona automaticamente.

**Propriedades CSS do botão de rolagem para cima e rolagem para baixo**

<table id="table_89561098E43D44C2865267687BBF38F4"> 
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
>O botão suporta o seletor de atributo `state`, que pode ser usado para aplicar capas diferentes aos estados dos botões `up`, `down`, `over` e `disabled`.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - configure os botões de rolagem que têm 28 x 32 pixels e têm arte-final diferente para cada estado:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
}
```

