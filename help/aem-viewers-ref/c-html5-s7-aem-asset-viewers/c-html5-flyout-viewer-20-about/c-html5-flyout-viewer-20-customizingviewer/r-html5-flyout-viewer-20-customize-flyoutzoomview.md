---
title: Exibição de zoom de imagem suspensa
description: A visualização principal consiste na imagem estática e na imagem com zoom mostrada na visualização da imagem suspensa. Também consiste na área de navegação de realce exibida sobre a imagem estática e na mensagem de dica mostrada na parte superior da imagem estática.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: c04c4b8f-4e63-4e84-98c0-aa0781608130
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 0%

---

# Exibição de zoom de imagem suspensa{#flyout-zoom-view}

A visualização principal consiste na imagem estática e na imagem com zoom mostrada na visualização da imagem suspensa. Também consiste na área de navegação de realce exibida sobre a imagem estática e na mensagem de dica mostrada na parte superior da imagem estática.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Se as dimensões da imagem que está sendo visualizada não corresponderem às dimensões da exibição de zoom da imagem suspensa, o conteúdo da imagem será centralizado na área de exibição do retângulo da exibição de zoom da imagem suspensa.

**Propriedades CSS da exibição principal**

A aparência da visualização principal é controlada com o seguinte seletor de classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p> A cor do plano de fundo da janela principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para tornar a exibição principal transparente:

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**Propriedades CSS da exibição da imagem suspensa**

A aparência da exibição de imagem suspensa é controlada com o seguinte seletor de classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> saiu de </span> </p> </td> 
   <td colname="col2"> <p> A posição horizontal da exibição da imagem suspensa, relativa ao canto superior esquerdo da exibição principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> A posição vertical da exibição da imagem suspensa, relativa ao canto superior esquerdo da exibição principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p> A largura da exibição da imagem suspensa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>A altura da exibição da imagem suspensa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borda </span> </p> </td> 
   <td colname="col2"> <p>A borda da exibição da imagem suspensa. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar uma exibição de imagem suspensa para 600 x 400 pixels, aparecendo com 100 pixels deslocados à direita da exibição principal de 512 x 288 mostrada no exemplo anterior:

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 left: 612px; 
 top: 0px; 
 width: 600px; 
 height: 400px;  
}
```

**Propriedades CSS do destaque na exibição principal**

A aparência do destaque na exibição principal é controlada com o seguinte seletor de classe CSS:

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight
```

É possível controlar o plano de fundo, a borda, a transparência e atributos semelhantes usando CSS. No entanto, o tamanho e a posição do elemento DOM de destaque são gerenciados pela lógica do visualizador. Não há suporte para a substituição por meio do CSS.

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p> A cor do destaque. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidade </span> </p> </td> 
   <td colname="col2"> <p> Realçar opacidade. </p> <p>Para o Internet Explorer 8, use <span class="codeph"> filter:alpha(opacity-...) ); </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borda </span> </p> </td> 
   <td colname="col2"> <p>O destaque da borda. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar um realce verde com 40% de transparência e uma borda vermelha de um pixel:

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight { 
 background-color: green; 
 opacity: 0.4;  
 filter: alpha(opacity = 40); 
 border: 1px solid red; 
}
```

**Propriedades CSS do cursor**

Quando o parâmetro `highlightmode` é definido como `cursor`, os realces estão na exibição principal são substituídos por um trabalho artístico de cursor de tamanho fixo, que é controlado com o seletor de classe CSS:

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7cursor
```

É possível controlar a imagem de fundo e o tamanho usando CSS.

As propriedades de CSS aplicáveis incluem:

<table id="table_A86F1E4DE9E84E11AF47373ADC63A459"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo </span> </p> </td> 
   <td colname="col2"> <p>Trabalho artístico de cursor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do cursor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do cursor. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>O cursor oferece suporte ao seletor de atributo `input`, que pode ser usado para aplicar arte-final e tamanho de cursor diferentes a dispositivos diferentes. Especificamente, `input="mouse"` corresponde aos sistemas de desktop e `input="touch"` corresponde aos dispositivos de toque.

**Propriedades CSS da sobreposição**

Quando o parâmetro `overlay` é definido como `1`, a área ao redor do quadro de realce ou da imagem do cursor é controlada com o seletor de classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p>Cor de sobreposição. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidade </span> </p> </td> 
   <td colname="col2"> <p>Opacidade de sobreposição. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Propriedades CSS da mensagem de dica**

A aparência da mensagem de dica é controlada com o seguinte seletor de classe CSS:

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

É possível configurar o estilo da fonte, o tamanho, a aparência e o deslocamento vertical por meio do CSS. No entanto, o alinhamento horizontal é gerenciado pela lógica do visualizador. Não há suporte para a substituição por CSS usando as propriedades `left` ou `right`.

<table id="table_DCF6B69A9D8C4DB7A10C4572F7484799"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> inferior </p> </td> 
   <td colname="col2"> <p>Deslocamento da parte inferior da exibição principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Família de fontes <span class="codeph"> </span> </p> </td> 
   <td colname="col2"> <p>Nome da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento ao redor do texto da mensagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p>Cor de preenchimento do fundo do texto da mensagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> raio da borda </span> </p> </td> 
   <td colname="col2"> <p>Raio da borda do fundo do texto da mensagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidade </span> </p> </td> 
   <td colname="col2"> <p>Opacidade do plano de fundo do texto da mensagem. </p> <p>Para o Internet Explorer 8, use <span class="codeph"> filter:alpha(opacity-...) ) </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

A mensagem de dica pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) para obter mais informações.

Exemplo - para configurar uma mensagem de dica semitransparente com fonte Arial® de 12 px branca, deslocamento de 50 pixels da parte inferior da exibição principal, preenchimento e uma borda arredondada:

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
