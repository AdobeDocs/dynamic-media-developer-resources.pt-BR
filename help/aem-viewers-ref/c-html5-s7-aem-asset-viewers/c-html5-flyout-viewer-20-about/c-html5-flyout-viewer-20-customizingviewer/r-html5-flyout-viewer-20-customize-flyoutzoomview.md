---
description: A visualização principal consiste na imagem estática, na imagem ampliada mostrada na visualização de flyout, na área de navegação de realce exibida sobre a imagem estática e na mensagem de dica mostrada sobre a imagem estática.
seo-description: A visualização principal consiste na imagem estática, na imagem ampliada mostrada na visualização de flyout, na área de navegação de realce exibida sobre a imagem estática e na mensagem de dica mostrada sobre a imagem estática.
seo-title: Visualização de zoom do menu suspenso
solution: Experience Manager
title: Visualização de zoom do menu suspenso
topic: Dynamic Media
uuid: 35c60228-3044-442b-a8e2-e13d0bd306a5
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 0%

---


# Visualização de zoom do Flyout{#flyout-zoom-view}

A visualização principal consiste na imagem estática, na imagem ampliada mostrada na visualização de flyout, na área de navegação de realce exibida sobre a imagem estática e na mensagem de dica mostrada sobre a imagem estática.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Se as dimensões da imagem que está sendo visualizada não corresponderem às dimensões da visualização de zoom flyout, o conteúdo da imagem será centralizado na área de exibição do retângulo de zoom flyout visualização.

**Propriedades de CSS da visualização principal**

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
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p> A cor de fundo da visualização principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para tornar a visualização principal transparente:

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**Propriedades de CSS da visualização flyout**

A aparência da visualização flyout é controlada com o seguinte seletor de classe CSS:

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
   <td colname="col2"> <p> A posição horizontal da visualização do flyout, em relação ao canto superior esquerdo da visualização principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> A posição vertical da visualização do flyout, em relação ao canto superior esquerdo da visualização principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> A largura da visualização flyout. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>A altura da visualização voadora. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fronteira  </span> </p> </td> 
   <td colname="col2"> <p>A borda da visualização do flyout. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar uma visualização de flyout para 600 x 400 pixels, que aparece com 100 pixels de deslocamento à direita da visualização principal 512 x 288 mostrada no exemplo anterior:

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 left: 612px; 
 top: 0px; 
 width: 600px; 
 height: 400px;  
}
```

**Propriedades de CSS do destaque na visualização principal**

A aparência do realce na visualização principal é controlada pelo seguinte seletor de classe CSS:

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight
```

É possível controlar o plano de fundo, a borda, a transparência e atributos semelhantes usando o CSS. No entanto, o tamanho e a posição do elemento DOM de realce são gerenciados pela lógica do visualizador. Não há suporte para substituí-lo pelo CSS.

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p> A cor do realce. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidade  </span> </p> </td> 
   <td colname="col2"> <p> Realce a opacidade. </p> <p>Para o Internet Explorer 8, use <span class="codeph"> filter:alpha(opacity-...) ); </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fronteira  </span> </p> </td> 
   <td colname="col2"> <p>O realce da borda. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar o realce verde com 40% de transparência e uma borda vermelha de um pixel:

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight { 
 background-color: green; 
 opacity: 0.4;  
 filter: alpha(opacity = 40); 
 border: 1px solid red; 
}
```

**Propriedades de CSS do cursor**

Quando o parâmetro `highlightmode` está definido como `cursor`, os realces estão na visualização principal e são substituídos pela arte-final do cursor de tamanho fixo, que é controlada pelo seletor de classe CSS:

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7cursor
```

É possível controlar a imagem e o tamanho do plano de fundo usando o CSS.

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
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
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
>O cursor oferece suporte ao seletor de atributos `input`, que pode ser usado para aplicar artes e tamanhos de cursor diferentes para dispositivos diferentes. Especificamente, `input="mouse"` corresponde aos sistemas de desktop e `input="touch"` corresponde aos dispositivos de toque.

**Propriedades de CSS da sobreposição**

Quando o parâmetro `overlay` estiver definido como `1`, a área em torno do quadro de realce ou da imagem do cursor será controlada com o seletor de classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p>Cor da sobreposição. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidade  </span> </p> </td> 
   <td colname="col2"> <p>Opacidade da sobreposição. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Propriedades de CSS da mensagem de dica**

A aparência da mensagem de dica é controlada com o seguinte seletor de classe CSS:

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

É possível configurar o estilo da fonte, a aparência do tamanho e o deslocamento vertical por meio do CSS. Entretanto, o alinhamento horizontal é gerenciado pela lógica do visualizador. Não há suporte para substituir por CSS usando as propriedades `left` ou `right`.

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
   <td colname="col2"> <p>Deslocamento na parte inferior da visualização principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor  </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes  </span> </p> </td> 
   <td colname="col2"> <p>Nome da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> revestimento  </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento em torno do texto da mensagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p>Cor de preenchimento do plano de fundo do texto da mensagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> raio da borda  </span> </p> </td> 
   <td colname="col2"> <p>Raio da borda do plano de fundo do texto da mensagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidade  </span> </p> </td> 
   <td colname="col2"> <p>Opacidade do texto da mensagem em segundo plano. </p> <p>Para o Internet Explorer 8, use <span class="codeph"> filter:alpha(opacity-...) ) </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

A mensagem de dica pode ser localizada. Consulte [Localização de elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) para obter mais informações.

Exemplo - para configurar uma mensagem de ponta semitransparente com fonte Arial branca de 12 px, 50 pixels de deslocamento a partir da parte inferior da visualização principal, preenchimento e uma borda arredondada:

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

