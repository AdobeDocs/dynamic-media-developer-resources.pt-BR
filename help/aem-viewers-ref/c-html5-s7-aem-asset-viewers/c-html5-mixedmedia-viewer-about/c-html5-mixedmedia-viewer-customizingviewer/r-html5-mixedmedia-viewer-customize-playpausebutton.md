---
description: O botão Reproduzir/pausar faz com que o reprodutor de vídeo reproduza ou pause o conteúdo do vídeo quando um usuário clicar nele.
solution: Experience Manager
title: Botão Reproduzir/Pausar
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídias mistas
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---


# Botão Reproduzir/Pausar{#play-pause-button}

O botão Reproduzir/pausar faz com que o reprodutor de vídeo reproduza ou pause o conteúdo do vídeo quando um usuário clicar nele.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

É possível dimensionar, usar a capa e posicionar o botão, em relação à barra de controle que o contém, por CSS.

O seguinte seletor de classe CSS controla a aparência do botão:

```
.s7mixedmediaviewer .s7playpausebutton
```

## Propriedades CSS do botão Reproduzir/Pausar {#css-properties-of-the-play-pause-button}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda superior, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda direita, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left  </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda esquerda, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p> Posição a partir da borda inferior, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo  </span> </p> </td> 
   <td colname="col2"> <p>A imagem exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esse botão suporta os seletores de atributos `state`, `selected` e `replay`, que podem ser usados para aplicar capas diferentes a estados de botão diferentes. Em particular, `selected='true'` corresponde ao estado &quot;reproduzir&quot; e `selected='false'` corresponde ao estado &quot;pausar&quot;;
>
>`replay='true'` é definido quando o vídeo atinge o fim, e clicar no botão reinicia a reprodução a partir do início.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) para obter mais informações.

## Exemplo {#section-e8caea0a303c425a8a637c2a47c06355}

Para configurar um botão reproduzir/pausar com 32 x 32 pixels; é posicionado seis pixels da borda superior e esquerda da barra de controle e exibe uma imagem diferente para cada um dos quatro estados de botão diferentes quando selecionado ou não selecionado.

```
.s7mixedmediaviewer .s7playpausebutton { 
top:6px; 
left:6px; 
width:32px; 
height:32px; 
} 
.s7mixedmediaviewer .s7playpausebutton[selected='true'][state='up'] { 
background-image:url(images/playBtn_up.png); 
} 
.s7mixedmediaviewer .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/playBtn_over.png); 
} 
.s7mixedmediaviewer .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/playBtn_down.png); 
} 
.s7mixedmediaviewer .s7playpausebutton[selected='true'][state='disabled'] { 
background-image:url(images/playBtn_disabled.png); 
} 
.s7mixedmediaviewer .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/pauseBtn_up.png); 
} 
.s7mixedmediaviewer .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/pauseBtn_over.png); 
} 
.s7mixedmediaviewer .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/pauseBtn_down.png); 
} 
.s7mixedmediaviewer .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/pauseBtn_disabled.png); } 
} 
.s7mixedmediaviewer .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/replayBtn_up.png); 
} 
.s7mixedmediaviewer .s7playpausebutton[selected='true'][replay='true'][state='over'] {  
background-image:url(images/replayBtn_over.png); 
} 
.s7mixedmediaviewer .s7playpausebutton[selected='true'][replay='true'][state='down'] {  
background-image:url(images/replayBtn_down.png); 
} 
.s7mixedmediaviewer .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/replayBtn_disabled.png); 
}
```

