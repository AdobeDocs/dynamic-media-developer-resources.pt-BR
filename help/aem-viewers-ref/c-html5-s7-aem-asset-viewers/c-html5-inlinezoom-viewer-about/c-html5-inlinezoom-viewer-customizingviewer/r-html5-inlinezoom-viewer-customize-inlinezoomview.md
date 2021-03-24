---
description: A exibição principal consiste na imagem estática, na imagem com zoom mostrada na exibição de flyout na parte superior da imagem estática e na mensagem de dica mostrada na parte superior da imagem estática.
solution: Experience Manager
title: Visualização de zoom de menu suspenso
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom em linha
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---


# Visualização de zoom de menu suspenso{#flyout-zoom-view}

A exibição principal consiste na imagem estática, na imagem com zoom mostrada na exibição de flyout na parte superior da imagem estática e na mensagem de dica mostrada na parte superior da imagem estática.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

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

A mensagem de dica pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) para obter mais informações.

.

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

