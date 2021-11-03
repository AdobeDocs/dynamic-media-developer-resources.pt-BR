---
title: Efeito de ícone
description: O ícone Reproduzir é sobreposto na área de visualização principal. Ele é exibido quando o vídeo é pausado ou quando o fim do vídeo é atingido, e também depende do parâmetro de efeito de ícone .
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: f4bf343a-4a78-470b-abe5-94e2d608f45d
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Efeito de ícone{#icon-effect}

O ícone Reproduzir é sobreposto na área de visualização principal. Ele é exibido quando o vídeo é pausado ou quando o fim do vídeo é atingido, e também depende do parâmetro de efeito de ícone .

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A aparência do ícone de reprodução é controlada com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer . s7smartcropvideoplayer .s7iconeffect
```

**Propriedades CSS do ícone de reprodução**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo </span> </p> </td> 
   <td colname="col2"> <p> A imagem exibida para o ícone de reprodução. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> A largura do ícone de reprodução. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>A altura do ícone de reprodução. </p> </td> 
  </tr> 
 </tbody> 
</table>

O efeito de ícone suporta `state` seletor de atributos. `state="play"` é usado quando o vídeo é pausado no meio da reprodução e `state="replay"` é usado quando o indicador de reprodução está no final do fluxo.

## Exemplo {#section-e8caea0a303c425a8a637c2a47c06355}

Configure um ícone de reprodução de 100 x 100 pixels.

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```
