---
description: O ícone Reproduzir é sobreposto na área de visualização de vídeo. Ele é exibido quando o vídeo é pausado ou quando o fim do vídeo é atingido, e também depende do parâmetro de efeito de ícone .
solution: Experience Manager
title: Efeito do ícone do reprodutor de vídeo
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídias mistas
role: Developer,Business Practitioner
exl-id: 1e0bd97f-20e9-41e6-95fc-d693644152da
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# Efeito do ícone do reprodutor de vídeo{#video-player-icon-effect}

O ícone Reproduzir é sobreposto na área de visualização de vídeo. Ele é exibido quando o vídeo é pausado ou quando o fim do vídeo é atingido, e também depende do parâmetro de efeito de ícone .

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A aparência do ícone de reprodução é controlada com o seguinte seletor de classe CSS:

```
.s7mixedmediaviewer . s7videoplayer .s7iconeffect
```

**Propriedades CSS do ícone de reprodução**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo  </span> </p> </td> 
   <td colname="col2"> <p> A imagem exibida para o ícone de reprodução. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
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

O efeito de ícone suporta o seletor de atributo `state`. `state="play"` é usado quando o vídeo é pausado no meio da reprodução e  `state="replay"` é usado quando o indicador de reprodução está no final do fluxo.

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
