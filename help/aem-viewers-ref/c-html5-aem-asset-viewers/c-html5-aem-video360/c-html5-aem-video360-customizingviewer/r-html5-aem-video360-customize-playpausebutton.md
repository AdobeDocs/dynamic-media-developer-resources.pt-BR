---
title: Botão Reproduzir/Pausar
description: O botão Reproduzir/pausar faz com que o reprodutor de vídeo reproduza ou pause o conteúdo do vídeo quando um usuário clica nele.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 5f8741a4-d286-4b2d-8a11-23bce119209a
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---

# Botão Reproduzir/Pausar{#play-pause-button}

O botão Reproduzir/pausar faz com que o reprodutor de vídeo reproduza ou pause o conteúdo do vídeo quando um usuário clica nele.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Você pode dimensionar, aplicar capa e posicionar o botão, em relação à barra de controle que o contém, por CSS.

O seletor de classe CSS a seguir controla a aparência do botão:

```
.s7video360viewer .s7playpausebutton
```

## Propriedades CSS do botão Reproduzir/pausar {#css-properties-of-the-play-pause-button}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda superior, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> direita </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda direita, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> saiu de </span> </p> </td> 
   <td colname="col2"> <p>Posição a partir da borda esquerda, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> inferior </p> </td> 
   <td colname="col2"> <p> Posição a partir da borda inferior, incluindo o preenchimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo </span> </p> </td> 
   <td colname="col2"> <p>A imagem exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão oferece suporte aos seletores de atributo `state`, `selected` e `replay`, que podem ser usados para aplicar capas diferentes a estados de botão diferentes. Especificamente, `selected='true'` corresponde ao estado &quot;play&quot; e `selected='false'` corresponde ao estado &quot;pause&quot;;
>
>O seletor de atributo `replay='true'` é definido quando o vídeo atinge o fim e selecionar o botão reinicia a reprodução do início.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) para obter mais informações.

**Exemplo** - Para configurar um botão Reproduzir/Pausar com 32 x 32 pixels. Posicionar seis pixels a partir da borda superior e esquerda da barra de controle. E, por fim, o exibe uma imagem diferente para cada um dos quatro estados de botão diferentes quando selecionados ou não selecionados.

```
.s7video360viewer .s7playpausebutton { 
top:6px; 
left:6px; 
width:32px; 
height:32px; 
} 
.s7video360viewer .s7playpausebutton[selected='true'][state='up'] { 
background-image:url(images/playBtn_up.png); 
} 
.s7video360viewer .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/playBtn_over.png); 
} 
.s7video360viewer .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/playBtn_down.png); 
} 
.s7video360viewer .s7playpausebutton[selected='true'][state='disabled'] { 
background-image:url(images/playBtn_disabled.png); 
} 
.s7video360viewer .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/pauseBtn_up.png); 
} 
.s7video360viewer .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/pauseBtn_over.png); 
} 
.s7video360viewer .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/pauseBtn_down.png); 
} 
.s7video360viewer .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/pauseBtn_disabled.png); } 
} 
.s7video360viewer .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/replayBtn_up.png); 
} 
.s7video360viewer .s7playpausebutton[selected='true'][replay='true'][state='over'] {  
background-image:url(images/replayBtn_over.png); 
} 
.s7video360viewer .s7playpausebutton[selected='true'][replay='true'][state='down'] {  
background-image:url(images/replayBtn_down.png); 
} 
.s7video360viewer .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/replayBtn_disabled.png); 
}
```
