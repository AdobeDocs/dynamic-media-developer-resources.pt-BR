---
description: No modo de zoom em linha, a exibição principal consiste na imagem estática, imagem com zoom mostrada na exibição de flyout sobre a imagem estática e a mensagem de dica mostrada sobre a imagem estática.
solution: Experience Manager
title: Exibição de Zoom do Flyout
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídias mistas
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---


# Exibição de Zoom do Flyout{#flyout-zoom-view}

No modo de zoom em linha, a exibição principal consiste na imagem estática, imagem com zoom mostrada na exibição de flyout sobre a imagem estática e a mensagem de dica mostrada sobre a imagem estática.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área principal do visualizador**

A aparência da exibição principal é controlada com o seguinte seletor de classe CSS:

```
.s7mixedmediaviewer .s7flyoutzoomview
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
.s7mixedmediaviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

<!--<a id="section_FD07AB77593748F99DC6C42ED20A61EC"></a>-->

A aparência da mensagem de dica é controlada com o seguinte seletor de classe CSS:

```
.s7mixedmediaviewer .s7flyoutzoomview .s7tip
```

É possível configurar o estilo da fonte, a aparência do tamanho e o deslocamento vertical por meio do CSS. No entanto, o alinhamento horizontal é gerenciado pela lógica do visualizador. Não há suporte para substituí-lo por meio de CSS usando propriedades `left` ou `right`.

**Propriedades CSS da mensagem de dica**

<table id="table_5417B0C0343747649502629F43DF231A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p>Cor de preenchimento do plano de fundo da mensagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> Raio da borda do fundo da mensagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p> Deslocamento na parte inferior da exibição principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto da dica. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte  </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes  </span> </p> </td> 
   <td colname="col2"> <p>Família de fontes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidade  </span> </p> </td> 
   <td colname="col2"> <p> Opacidade do plano de fundo da mensagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento  </span> </p> </td> 
   <td colname="col2"> <p> Preenchimento em torno do texto da mensagem. </p> </td> 
  </tr> 
 </tbody> 
</table>

A mensagem de dica pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) para obter mais informações.

Exemplo - Para configurar uma mensagem de ponta semitransparente com fonte branca Arial 12px, 50 pixels são deslocados a partir da parte inferior da exibição principal, no preenchimento e em uma borda arredondada:

```
.s7mixedmediaviewer .s7flyoutzoomview .s7tip { 
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

