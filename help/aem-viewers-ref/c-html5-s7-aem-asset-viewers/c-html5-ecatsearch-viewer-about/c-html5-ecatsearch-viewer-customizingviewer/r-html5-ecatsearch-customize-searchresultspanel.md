---
title: Painel de resultados da pesquisa
description: O painel de resultados da pesquisa consiste na caixa de entrada de pesquisa na parte superior e na área principal onde as mensagens informativas ou os resultados da pesquisa são exibidos.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: ffbbc2ae-60da-4c3d-a350-6dbcb64e189d
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '925'
ht-degree: 0%

---

# Painel de resultados da pesquisa{#search-results-panel}

O painel de resultados da pesquisa consiste na caixa de entrada de pesquisa na parte superior e na área principal onde as mensagens informativas ou os resultados da pesquisa são exibidos.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área do visualizador principal**

Quando o painel está ativo, a interface do usuário do visualizador é coberta por um preenchimento semitransparente. A cor e a opacidade desse preenchimento são controladas com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7searchpanel .s7backoverlay
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Cor da sobreposição. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidade </span> </p> </td> 
   <td colname="col2"> <p>Opacidade da cor. </p> </td> 
  </tr> 
 </tbody> 
</table>

O painel de resultados da pesquisa sempre ocupa toda a altura do visualizador disponível. No entanto, você pode configurar a largura. Você pode definir a largura como um valor de pixel absoluto, que é uma configuração padrão para pontos de interrupção de tamanho médio e grande. Ou você pode definir a largura como 100% para que o painel de resultados da pesquisa ocupe toda a área do visualizador. A largura do painel é controlada pelo seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchresultspace
```

**Propriedade CSS do espaço de resultados da pesquisa**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p> Largura do espaço do resultado da pesquisa. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar um painel de resultados de pesquisa com largura de 250 pixels em pontos de interrupção grandes e médios e usar um painel de tamanho normal em um ponto de interrupção de tamanho pequeno:

```
.s7ecatalogsearchviewer.s7size_large .s7searchpanel .s7searchresultspanel, .s7ecatalogsearchviewer.s7size_medium .s7searchpanel .s7searchresultspanel { 
 width:250px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7searchpanel .s7searchresultspanel { 
 width:100%; 
}
```

A parte superior do painel de resultados da pesquisa é dedicada à caixa de entrada de pesquisa. O preenchimento nas laterais da caixa de entrada é controlado pelo seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputcontainer
```

**Propriedades CSS do contêiner de entrada de pesquisa**

<table id="table_A1B96108542742DC8DCBCC9064F9E90B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p> Preenchimento ao redor da caixa de entrada. </p> </td> 
  </tr> 
 </tbody> 
</table>

O campo de entrada de pesquisa é controlado pelo seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput
```

**Propriedades CSS do campo de entrada de pesquisa**

<table id="table_9FB5E89847BF4C889DC22AD7E842C0F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do campo de entrada de pesquisa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento à esquerda </span> </p> </td> 
   <td colname="col2"> <p> O preenchimento interno entre os limites do campo de entrada e o texto de entrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borda </span> </p> </td> 
   <td colname="col2"> <p>Borda do campo de entrada de pesquisa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem </span> </p> </td> 
   <td colname="col2"> <p>Margem do campo de entrada de pesquisa </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte do texto. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar um campo de entrada de pesquisa com altura de 0 pixel e fonte de texto de 14 pixels:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput { 
 padding-left:5px; 
 height:30px; 
 font-size:14px; 
}
```

O botão de pesquisa à esquerda do campo de entrada de pesquisa na forma de &quot;espelho&quot; por padrão é controlado pelo seguinte seletor de classe CSS:

```
 .s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton
```

**Propriedades CSS do botão de entrada de pesquisa**

<table id="table_CDD818B40BB1416CB47B7C52F799DE0C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão de entrada de pesquisa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão de entrada de pesquisa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>O URL para a imagem do ícone "espelho". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-size </span> </p> </td> 
   <td colname="col2"> <p>O tamanho do ícone "espelho". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borda </span> </p> </td> 
   <td colname="col2"> <p>Borda do botão de entrada de pesquisa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem </span> </p> </td> 
   <td colname="col2"> <p>Margem do botão de entrada de pesquisa. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - Para configurar um botão de pesquisa com 26 x 26 pixels ícone de &quot;espelho&quot;; 30 pixels de tamanho com uma borda de 1 pixel:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton { 
 width:30px; 
 height:30px; 
 background-size:26px 26px; 
 background-image: url(images/v2/Search_form_field.png); 
 font-size:14px; 
 border: 1px solid #696969; 
}
```

O painel de resultados da pesquisa pode exibir um prompt textual quando o recurso é chamado pela primeira vez. E também mostra uma mensagem quando a pesquisa de um usuário não retornou resultados. Em todos os casos, o texto é exibido na parte principal do painel de resultados da pesquisa e é controlado pelo seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo
```

**Propriedades CSS das informações de pesquisa**

<table id="table_1DF5A12A21584FCC8C25F170078FEFE6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor </span> </p> </td> 
   <td colname="col2"> <p> Cor do texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Nome da fonte do texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align </span> </p> </td> 
   <td colname="col2"> <p>Alinhamento de texto horizontal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Tamanho do texto da fonte. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esse painel de texto oferece suporte à `state` seletor de atributo, que pode ser usado para aplicar estilos diferentes a mensagens de texto diferentes. Em especial, `state='prompt'` corresponde à solicitação de texto exibida quando o painel é chamado pela primeira vez. A variável `state='results'` corresponde ao texto com informações sobre ocorrências de pesquisa. E, finalmente, o `state='no_results'` corresponde ao texto mostrado quando a consulta de pesquisa não retornou resultados.

O texto da mensagem pode ser localizado. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - Para configurar um painel de texto que use uma fonte cinza de 18 pixels:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo { 
 font-size: 18px; 
 color: #696969; 
}
```

Os resultados da pesquisa são renderizados como uma única coluna ou linha de miniaturas para páginas com ocorrências de pesquisa. O espaçamento entre as miniaturas dos resultados da pesquisa é controlado com o seguinte seletor de classe CSS:

```
.ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell
```

**Propriedades CSS das células em miniatura**

<table id="table_26974E509F6943BB98CBC1E4BAE62D68"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem </span> </p> </td> 
   <td colname="col2"> <p> O tamanho da margem vertical ao redor de cada miniatura. O espaçamento real da miniatura é igual à soma das margens superior e inferior definidas para <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - Para configurar o espaçamento de dez pixels:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

A aparência de miniaturas individuais é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb
```

**Propriedades CSS da miniatura**

<table id="table_00829E44F75040A4B2AE19ACD550DA1E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura da miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura da miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borda </span> </p> </td> 
   <td colname="col2"> <p>Borda da miniatura. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - Para configurar miniaturas com 215 x 129 pixels, tenha uma borda padrão cinza-claro e uma borda selecionada cinza-escuro:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb { 
 width: 215px; 
 height: 129px; 
}
```

A aparência do rótulo da miniatura é controlada com o seguinte seletor de classe CSS:

```
 .s7ecatalogsearchviewer 
.s7searchpanel .s7swatches .s7label
```

**Propriedades CSS do rótulo**

<table id="table_CA669F6AE7574FF389BF725B3F768E5E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor </span> </p> </td> 
   <td colname="col2"> <p> Cor do texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Nome da fonte do texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte do texto. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - Para configurar rótulos que usam fonte de 12 pixels, cinza e Helvetica®:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7label { 
 font-family: Helvetica,sans-serif; 
 color: #4c4c4c; 
 font-size: 12px; 
}
```

Em sistemas que usam entrada de mouse, dois botões de rolagem são exibidos na parte inferior do painel de resultados da pesquisa para um usuário rolar pelos resultados da pesquisa. A aparência dos botões de rolagem para cima e para baixo é controlada com os seguintes seletores de classe CSS:

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton
```

Não é possível posicionar botões de rolagem usando as propriedades CSS top, left, bottom e right. Em vez disso, a lógica do visualizador as posiciona automaticamente.

**Propriedades CSS dos botões de rolagem para cima e para baixo**

<table id="table_11063C7F428D4707A8138F17650F8F5F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão de rolagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão de rolagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> A imagem exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esse botão oferece suporte ao `state` seletor de atributo, que pode ser usado para aplicar capas diferentes a `"up"`, `"down"`, `"over"`, e `"disabled"` estados do botão.

As dicas de ferramentas do botão podem ser localizadas. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - Para configurar um botão de rolagem para cima com 125 x 35 pixels e que tenha um trabalho artístico diferente para cada estado:

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton { 
 width:125px; 
 height:35px; 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='up'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_up.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_over.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_down.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_disabled.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton { 
 width:125px; 
 height:35px; 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_up.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_over.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_down.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_disabled.png);
```
