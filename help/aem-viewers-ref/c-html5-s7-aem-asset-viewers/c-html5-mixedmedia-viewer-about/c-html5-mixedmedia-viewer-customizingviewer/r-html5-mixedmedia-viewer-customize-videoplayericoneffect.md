---
description: O ícone de reprodução é sobreposto na área de visualização do vídeo. Ele é exibido quando o vídeo é pausado ou quando o fim do vídeo é atingido, e também depende do parâmetro de efeito de ícone.
seo-description: O ícone de reprodução é sobreposto na área de visualização do vídeo. Ele é exibido quando o vídeo é pausado ou quando o fim do vídeo é atingido, e também depende do parâmetro de efeito de ícone.
seo-title: Efeito ícone do player de vídeo
solution: Experience Manager
title: Efeito ícone do player de vídeo
topic: Dynamic Media
uuid: 5d59c4b2-a7a1-49e1-84c7-0e127a571c4f
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---


# Efeito do ícone do player de vídeo{#video-player-icon-effect}

O ícone de reprodução é sobreposto na área de visualização do vídeo. Ele é exibido quando o vídeo é pausado ou quando o fim do vídeo é atingido, e também depende do parâmetro de efeito de ícone.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A aparência do ícone play é controlada pelo seguinte seletor de classe CSS:

```
.s7mixedmediaviewer . s7videoplayer .s7iconeffect
```

**Propriedades de CSS do ícone de reprodução**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> A imagem exibida para o ícone Reproduzir. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da sprite de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> A largura do ícone de reprodução. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>A altura do ícone de reprodução. </p> </td> 
  </tr> 
 </tbody> 
</table>

O efeito Ícone suporta o seletor de atributos `state`. `state="play"` é usado quando o vídeo é pausado no meio da reprodução e  `state="replay"` é usado quando o indicador de reprodução está no final do fluxo.

## Exemplo {#section-e8caea0a303c425a8a637c2a47c06355}

Configure um ícone de reprodução de 100 x 100 pixels.

```
.s7mixedmediaviewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7mixedmediaviewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7mixedmediaviewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```

