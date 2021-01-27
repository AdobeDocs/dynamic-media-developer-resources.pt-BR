---
description: A visualização principal do modo de zoom em linha consiste na imagem estática, imagem com zoom exibida na visualização flyout sobre a imagem estática e a mensagem de dica mostrada sobre a imagem estática.
seo-description: A visualização principal do modo de zoom em linha consiste na imagem estática, imagem com zoom exibida na visualização flyout sobre a imagem estática e a mensagem de dica mostrada sobre a imagem estática.
seo-title: Visualização de zoom do menu suspenso
solution: Experience Manager
title: Visualização de zoom do menu suspenso
topic: Dynamic Media
uuid: c4c94432-7b6f-40a8-ae5f-9423234f3656
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---


# Visualização de zoom do menu suspenso{#flyout-zoom-view}

A visualização principal do modo de zoom em linha consiste na imagem estática, imagem com zoom exibida na visualização flyout sobre a imagem estática e a mensagem de dica mostrada sobre a imagem estática.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades de CSS da área do visualizador principal**

A aparência da visualização principal é controlada com o seguinte seletor de classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p> A cor de fundo da visualização principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para tornar a visualização principal transparente:

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

É possível configurar o estilo da fonte, a aparência do tamanho e o deslocamento vertical por meio do CSS. Entretanto, o alinhamento horizontal é gerenciado pela lógica do visualizador. Não há suporte para substituir por CSS usando as propriedades `left` ou `right`.

**Propriedades de CSS da mensagem de dica**

<table id="table_5417B0C0343747649502629F43DF231A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p>Cor de preenchimento do plano de fundo da mensagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> raio da borda  </span> </p> </td> 
   <td colname="col2"> <p> Raio da borda do plano de fundo da mensagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p> Deslocamento na parte inferior da visualização principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor  </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto da dica. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes  </span> </p> </td> 
   <td colname="col2"> <p>Família de fontes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidade  </span> </p> </td> 
   <td colname="col2"> <p> Opacidade em segundo plano da mensagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> revestimento  </span> </p> </td> 
   <td colname="col2"> <p> Preenchimento em torno do texto da mensagem. </p> </td> 
  </tr> 
 </tbody> 
</table>

A mensagem de dica pode ser localizada. Consulte [Localização de elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) para obter mais informações.

Exemplo - Para configurar uma mensagem de ponta semitransparente com fonte Arial branca de 12 pixels, o deslocamento de 50 pixels é feito na parte inferior da visualização principal, no preenchimento e em uma borda arredondada:

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

