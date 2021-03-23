---
description: O ícone Reproduzir é sobreposto na área de visualização principal. Ele é exibido quando o vídeo é pausado ou quando o fim do vídeo é atingido, e também depende do parâmetro de efeito de ícone .
seo-description: O ícone Reproduzir é sobreposto na área de visualização principal. Ele é exibido quando o vídeo é pausado ou quando o fim do vídeo é atingido, e também depende do parâmetro de efeito de ícone .
seo-title: Efeito de ícone
solution: Experience Manager
title: Efeito de ícone
uuid: a1e7d877-097c-4f43-8a6d-9627dc4924b1
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo 360 VR
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---


# Efeito de ícone{#icon-effect}

O ícone Reproduzir é sobreposto na área de visualização principal. Ele é exibido quando o vídeo é pausado ou quando o fim do vídeo é atingido, e também depende do parâmetro de efeito de ícone .

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A aparência do ícone de reprodução é controlada com o seguinte seletor de classe CSS:

```
.s7video360viewer . s7video360player .s7iconeffect
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
   <td colname="col2"> <p> Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
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

**Exemplo**  - Configure um ícone de reprodução de 100 x 100 pixels.

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

