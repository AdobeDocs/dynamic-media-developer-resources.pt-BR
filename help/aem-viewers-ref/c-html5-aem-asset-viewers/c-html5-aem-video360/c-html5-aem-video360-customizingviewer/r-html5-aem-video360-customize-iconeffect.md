---
title: Efeito do ícone
description: O ícone de reprodução é sobreposto na área de exibição principal. É exibido quando o vídeo é pausado ou quando o fim do vídeo é atingido, e também depende do parâmetro iconeffect.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: e25a3b9d-88ef-4214-9b6b-2527ebf0f145
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---

# Efeito do ícone{#icon-effect}

O ícone de reprodução é sobreposto na área de exibição principal. É exibido quando o vídeo é pausado ou quando o fim do vídeo é atingido, e também depende do parâmetro iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A aparência do ícone de reprodução é controlada com o seguinte seletor de classe CSS:

```
.s7video360viewer . s7video360player .s7iconeffect
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
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
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

O efeito de ícone oferece suporte ao seletor de atributos `state`. O seletor de atributo `state="play"` é usado quando o vídeo é pausado no meio da reprodução, e `state="replay"` é usado quando o indicador de reprodução está no final do fluxo.

**Exemplo** - Configurar um ícone de reprodução de 100 x 100 pixels.

```
.s7video360viewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7video360viewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7video360viewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```
