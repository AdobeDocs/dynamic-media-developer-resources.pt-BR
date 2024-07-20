---
title: Efeito do ícone
description: O indicador de zoom é sobreposto na área de exibição principal. Ela é exibida quando a imagem está em um estado redefinido e também depende do parâmetro iconeffect.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: fee22d02-172c-4f82-9b6c-e06db530f400
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---

# Efeito do ícone{#icon-effect}

O indicador de zoom é sobreposto na área de exibição principal. Ela é exibida quando a imagem está em um estado redefinido e também depende do parâmetro iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A aparência da área de visualização é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7pageview .s7iconeffect
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
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do indicador de zoom em pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do indicador de zoom em pixels. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>O efeito de ícone oferece suporte ao seletor de atributos `media-type`, que você pode usar para aplicar diferentes efeitos de ícone em diferentes dispositivos. Especificamente, `media-type='standard'` corresponde a sistemas desktop nos quais a entrada de mouse é normalmente usada e `media-type='multitouch'` corresponde a dispositivos com entrada de toque.

Exemplo - para configurar um indicador de zoom de 100 x 100 pixels com arte diferente para sistemas de desktop e dispositivos de toque.

```
.s7ecatalogviewer .s7pageview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7ecatalogviewer .s7pageview .s7iconeffect[media-type='standard'] { 
 background-image:url(images/v2/IconEffect_zoom.png); 
} 
.s7ecatalogviewer .s7pageview .s7iconeffect[media-type='multitouch'] { 
 background-image:url(images/v2/IconEffect_pinch.png); 
}
```
