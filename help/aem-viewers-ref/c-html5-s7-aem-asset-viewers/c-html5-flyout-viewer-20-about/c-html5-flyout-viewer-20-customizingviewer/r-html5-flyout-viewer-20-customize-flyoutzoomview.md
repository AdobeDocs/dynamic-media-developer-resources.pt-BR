---
description: A exibição principal consiste na imagem estática, na imagem com zoom mostrada na exibição do flyout, na área de navegação do destaque exibida sobre a imagem estática e na mensagem de dica mostrada sobre a imagem estática.
solution: Experience Manager
title: Visualização de zoom de menu suspenso
feature: Dynamic Media Classic,Visualizadores,SDK/API,Flyout
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 0%

---


# Visualização de zoom de menu suspenso{#flyout-zoom-view}

A exibição principal consiste na imagem estática, na imagem com zoom mostrada na exibição do flyout, na área de navegação do destaque exibida sobre a imagem estática e na mensagem de dica mostrada sobre a imagem estática.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Se as dimensões da imagem que está sendo visualizada não corresponderem às dimensões da exibição de zoom do flyout, o conteúdo da imagem será centralizado na área de exibição do retângulo da exibição de zoom do flyout.

**Propriedades CSS da exibição principal**

A aparência da exibição principal é controlada com o seguinte seletor de classe CSS:

```
.s7flyoutviewer .s7flyoutzoomview
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
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p> A cor de plano de fundo da exibição principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para tornar a exibição principal transparente:

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**Propriedades de CSS da exibição de flyout**

A aparência da exibição do flyout é controlada com o seguinte seletor de classe CSS:

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom
```

<table id="table_85446C72FD914594B7D108381BBFC673"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left  </span> </p> </td> 
   <td colname="col2"> <p> A posição horizontal da exibição do flyout, em relação ao canto superior esquerdo da exibição principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> A posição vertical da exibição do flyout, em relação ao canto superior esquerdo da exibição principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> A largura da exibição do flyout. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>A altura da exibição do flyout. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>A borda da exibição do flyout. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar uma exibição de flyout para 600 x 400 pixels, que aparece com deslocamento de 100 pixels à direita da exibição principal de 512 x 288 mostrada no exemplo anterior:

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 left: 612px; 
 top: 0px; 
 width: 600px; 
 height: 400px;  
}
```

**Propriedades CSS do destaque na exibição principal**

A aparência do realce na exibição principal é controlada com o seguinte seletor de classe CSS:

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight
```

É possível controlar o plano de fundo, a borda, a transparência e atributos semelhantes usando CSS. No entanto, o tamanho e a posição do elemento DOM de destaque são gerenciados pela lógica do visualizador. Não há suporte para substituí-lo por CSS.

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p> A cor do destaque. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidade  </span> </p> </td> 
   <td colname="col2"> <p> Realce a opacidade. </p> <p>Para o Internet Explorer 8, use <span class="codeph"> filter:alpha(opacity-...) ); </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>O realce da borda. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar um realce verde com transparência de 40% e uma borda vermelha de um pixel:

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight { 
 background-color: green; 
 opacity: 0.4;  
 filter: alpha(opacity = 40); 
 border: 1px solid red; 
}
```

**Propriedades CSS do cursor**

Quando o parâmetro `highlightmode` é definido como `cursor`, os realces estão na exibição principal e são substituídos por uma arte-final de cursor de tamanho fixo, que é controlada pelo seletor de classe CSS:

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7cursor
```

É possível controlar a imagem de fundo e o tamanho usando CSS.

As propriedades CSS aplicáveis incluem:

<table id="table_A86F1E4DE9E84E11AF47373ADC63A459"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo  </span> </p> </td> 
   <td colname="col2"> <p>Arte do cursor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Largura do cursor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do cursor. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>O cursor suporta o seletor de atributo `input`, que pode ser usado para aplicar arte-final de cursor e tamanho diferentes para dispositivos diferentes. Especificamente, `input="mouse"` corresponde aos sistemas de desktop e `input="touch"` corresponde aos dispositivos de toque.

**Propriedades CSS da sobreposição**

Quando o parâmetro `overlay` é definido como `1`, a área em torno do quadro de realce ou da imagem do cursor é controlada com o seletor de classe CSS:

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7overlay
```

<table id="table_A50CA8213C3A4682A081D3D30089574C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p>Cor da sobreposição. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidade  </span> </p> </td> 
   <td colname="col2"> <p>Opacidade de sobreposição. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Propriedades CSS da mensagem de dica**

A aparência da mensagem de dica é controlada com o seguinte seletor de classe CSS:

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

É possível configurar o estilo da fonte, a aparência do tamanho e o deslocamento vertical por meio do CSS. No entanto, o alinhamento horizontal é gerenciado pela lógica do visualizador. Não há suporte para substituí-lo por meio de CSS usando propriedades `left` ou `right`.

<table id="table_DCF6B69A9D8C4DB7A10C4572F7484799"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Deslocamento na parte inferior da exibição principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes  </span> </p> </td> 
   <td colname="col2"> <p>Nome da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte  </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento  </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento em torno do texto da mensagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p>Cor de preenchimento do plano de fundo do texto da mensagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p>Raio da borda do plano de fundo do texto da mensagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidade  </span> </p> </td> 
   <td colname="col2"> <p>Opacidade do texto da mensagem em segundo plano. </p> <p>Para o Internet Explorer 8, use <span class="codeph"> filter:alpha(opacity-...) ) </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

A mensagem de dica pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) para obter mais informações.

Exemplo - para configurar uma mensagem de ponta semitransparente com fonte branca Arial 12px, 50 pixels deslocados da parte inferior da exibição principal, preenchimento e uma borda arredondada:

```
.s7flyoutviewer .s7flyoutzoomview .s7tip { 
bottom: 50px; 
color: #ffffff; 
font-family: Arial; 
font-size: 12px; 
padding-bottom: 10px; 
padding-top: 10px; 
padding-left: 12px; 
padding-right: 12px; 
background-color: #000000; 
border-radius: 4px; 
opacity: 0.5; 
filter: alpha(opacity = 50); 
}
```

