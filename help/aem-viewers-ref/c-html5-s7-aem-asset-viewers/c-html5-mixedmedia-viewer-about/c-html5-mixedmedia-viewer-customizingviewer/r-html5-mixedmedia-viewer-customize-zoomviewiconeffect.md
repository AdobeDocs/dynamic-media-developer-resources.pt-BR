---
title: Efeito de ícone da exibição de zoom
description: O indicador de zoom é sobreposto na área de exibição de zoom. Ela é exibida quando a imagem está em um estado redefinido e também depende do parâmetro iconeffect.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: f2db0259-f1cf-41bc-86fd-97a40d01db16
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# Efeito de ícone da exibição de zoom{#zoom-view-icon-effect}

O indicador de zoom é sobreposto na área de exibição de zoom. Ela é exibida quando a imagem está em um estado redefinido e também depende do parâmetro iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área do visualizador principal**

A aparência da área de visualização é controlada com o seguinte seletor de classe CSS:

```
.s7mixedmediaviewer .s7zoomview .s7iconeffect
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
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo </span> </p> </td> 
   <td colname="col2"> <p> Arte do indicador de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do indicador de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do indicador de zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>O efeito de ícone oferece suporte ao seletor de atributos `media-type`, que você pode usar para aplicar diferentes efeitos de ícone em diferentes dispositivos. Especificamente, `media-type='standard'` corresponde a sistemas desktop nos quais a entrada de mouse é normalmente usada e `media-type='multitouch'` corresponde a dispositivos com entrada de toque.

Exemplo - para configurar um indicador de zoom de 100 x 100 pixels com arte diferente para sistemas de desktop e dispositivos de toque.

```
.s7mixedmediaviewer .s7zoomview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7mixedmediaviewer .s7zoomview .s7iconeffect[media-type='standard'] { 
 background-image:url(images/v2/IconEffect_zoom.png); 
} 
.s7mixedmediaviewer .s7zoomview .s7iconeffect[media-type='multitouch'] { 
 background-image:url(images/v2/IconEffect_pinch.png); 
}
```
