---
description: O visualizador exibe ícones de pontos de conexão sobre a visualização principal em lugares onde os pontos de conexão foram originalmente criados no Dynamic Media do AEM Assets - sob demanda.
seo-description: O visualizador exibe ícones de pontos de conexão sobre a visualização principal em lugares onde os pontos de conexão foram originalmente criados no Dynamic Media do AEM Assets - sob demanda.
seo-title: Pontos de conexão
solution: Experience Manager
title: Pontos de conexão
topic: Dynamic Media
uuid: 79c4d128-e24a-43b0-8e18-13b588eb396e
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# Pontos de conexão{#hotspots}

O visualizador exibe ícones de pontos de conexão sobre a visualização principal em lugares onde os pontos de conexão foram originalmente criados no Dynamic Media do AEM Assets - sob demanda.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades de CSS da área do visualizador principal**

A aparência do ícone do ponto de conexão é controlada com o seguinte seletor de classe CSS:

```
.s7interactiveimage .s7imagemapeffect .s7icon
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
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Arte-final do ícone de ponto de acesso. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p>Posição dentro da sprite de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largura do ícone do ponto de acesso. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do ícone do ponto de acesso. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - configure um ícone de ponto de acesso de 56 x 56 pixels que exibe uma imagem diferente para cada um dos dois estados de ícone diferentes:

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
 width: 56px; 
 height: 56px; 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

