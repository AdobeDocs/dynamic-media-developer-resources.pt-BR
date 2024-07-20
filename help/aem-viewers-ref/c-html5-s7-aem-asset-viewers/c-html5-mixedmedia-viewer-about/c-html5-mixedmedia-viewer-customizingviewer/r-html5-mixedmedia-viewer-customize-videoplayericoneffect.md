---
title: Efeito do ícone do reprodutor de vídeo
description: O ícone Reproduzir é sobreposto na área de visualização do vídeo. É exibido quando o vídeo é pausado ou quando o fim do vídeo é atingido, e também depende do parâmetro iconeffect.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1e0bd97f-20e9-41e6-95fc-d693644152da
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---

# Efeito do ícone do reprodutor de vídeo{#video-player-icon-effect}

O ícone Reproduzir é sobreposto na área de visualização do vídeo. É exibido quando o vídeo é pausado ou quando o fim do vídeo é atingido, e também depende do parâmetro iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A aparência do ícone de reprodução é controlada com o seguinte seletor de classe CSS:

```
.s7mixedmediaviewer . s7videoplayer .s7iconeffect
```

**Propriedades CSS do ícone de reprodução**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo </span> </p> </td> 
   <td colname="col2"> <p> A imagem exibida para o ícone de reprodução. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p> A largura do ícone de reprodução. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>A altura do ícone de reprodução. </p> </td> 
  </tr> 
 </tbody> 
</table>

O efeito de ícone oferece suporte ao seletor de atributos `state`. O seletor `state="play"` é usado quando o vídeo é pausado no meio da reprodução, e `state="replay"` é usado quando o indicador de reprodução está no final do fluxo.

## Exemplo {#section-e8caea0a303c425a8a637c2a47c06355}

Configurar um ícone de reprodução de 100 x 100 pixels.

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
