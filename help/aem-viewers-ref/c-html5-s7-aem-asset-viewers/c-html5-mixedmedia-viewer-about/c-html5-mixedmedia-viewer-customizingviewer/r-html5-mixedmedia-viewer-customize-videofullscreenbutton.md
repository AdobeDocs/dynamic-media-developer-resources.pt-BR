---
description: O botão de tela cheia faz com que o visualizador entre ou saia do modo de tela cheia quando clicado pelo usuário. Ele é usado quando o visualizador está exibindo o vídeo e está localizado na barra de controle. Esse botão não será exibido se o visualizador funcionar no modo pop-up e o sistema não oferecer suporte a tela cheia nativa.
seo-description: O botão de tela cheia faz com que o visualizador entre ou saia do modo de tela cheia quando clicado pelo usuário. Ele é usado quando o visualizador está exibindo o vídeo e está localizado na barra de controle. Esse botão não será exibido se o visualizador funcionar no modo pop-up e o sistema não oferecer suporte a tela cheia nativa.
seo-title: Botão Vídeo em tela cheia
solution: Experience Manager
title: Botão Vídeo em tela cheia
topic: Dynamic Media
uuid: f264154b-eb4d-4dcb-b8c0-e06c383198ae
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---


# Botão Vídeo em tela cheia{#video-full-screen-button}

O botão de tela cheia faz com que o visualizador entre ou saia do modo de tela cheia quando clicado pelo usuário. Ele é usado quando o visualizador está exibindo o vídeo e está localizado na barra de controle. Esse botão não será exibido se o visualizador funcionar no modo pop-up e o sistema não oferecer suporte a tela cheia nativa.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

É possível dimensionar, exibir a capa e posicionar o botão de tela inteira, em relação à barra de controle que a contém, por CSS.

A aparência do botão de tela cheia é controlada com o seletor de classe CSS:

```
.s7mixedmediaviewer .s7fullscreenbutton
```

**Propriedades de CSS do botão de tela cheia**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> Posição a partir da borda superior, incluindo preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p> Posição a partir da borda direita, incluindo preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left  </span> </p> </td> 
   <td colname="col2"> <p> Posição a partir da borda esquerda, incluindo preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda inferior, incluindo preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> A largura do botão de tela cheia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>A altura do botão de tela cheia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> A imagem exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da sprite de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão suporta os seletores de atributos `state` e `selected`, que podem ser usados para aplicar diferentes capas a diferentes estados de botão. Especificamente, `selected='true'` corresponde ao estado de &quot;tela cheia&quot; e `selected='false'` corresponde ao estado &quot;normal&quot;.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização de elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) para obter mais informações.

## Exemplo {#section-e8caea0a303c425a8a637c2a47c06355}

Para configurar um botão de tela cheia com 32 x 32 pixels e posicionado 6 pixels a partir da borda superior e direita da barra de controle. Além disso, exibe uma imagem diferente para cada um dos quatro estados de botão diferentes quando selecionado ou não selecionado.

```
.s7mixedmediaviewer . s7fullscreenbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='up'] { 
background-image:url(images/enterFullBtn_up.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='over'] {  
background-image:url(images/enterFullBtn_over.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='down'] {  
background-image:url(images/enterFullBtn_down.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='disabled'] { 
background-image:url(images/enterFullBtn_disabled.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='up'] {  
background-image:url(images/exitFullBtn_up.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='over'] {  
background-image:url(images/exitFullBtn_over.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='down'] {  
background-image:url(images/exitFullBtn_down.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='disabled'] {  
background-image:url(images/exitFullBtn_disabled.png); } 
}
```

