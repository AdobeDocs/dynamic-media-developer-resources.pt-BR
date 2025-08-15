---
title: Pontos de acesso e mapas de imagem
description: O visualizador exibe ícones de ponto de acesso sobre a exibição principal em locais onde os pontos de acesso foram originalmente criados no Dynamic Media do AEM Assets - sob demanda.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 70517201-9d59-4d9c-986d-a6e9655b7956
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---

# Pontos de acesso e mapas de imagem{#hotspots-and-image-maps}

O visualizador exibe ícones de ponto de acesso sobre a exibição principal em locais onde os pontos de acesso foram originalmente criados no Dynamic Media do AEM Assets - sob demanda.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área do visualizador principal**

A aparência do ícone de ponto de acesso é controlada com o seguinte seletor de classe CSS:

```
.s7carouselviewer .s7imagemapeffect .s7icon
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
   <td colname="col2"> <p>Arte do ícone do ponto de acesso. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>Posicione dentro da imagem do trabalho artístico, se as imagens CSS forem usadas. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do ícone de ponto de acesso. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do ícone do ponto de acesso. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - configure um ícone de ponto de acesso de 56 x 56 pixels que exiba uma imagem diferente para cada um dos dois estados de ícone diferentes:

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

<!--<a id="section_26D0B8444D1F42D493793FF54968C0B9"></a>-->

**Propriedades CSS da região do mapa de imagem**

A aparência da região do mapa de imagem é controlada com o seguinte seletor de classe CSS:

`.s7carouselviewer .s7imagemapeffect .s7region`

<table id="table_DAE7A78AA4A74DC78B2D94F29E8E236B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> plano de fundo </span> </p> </td> 
   <td colname="col2"> <p>Cor de preenchimento da região do mapa de imagem. </p> <p>Especifique esta cor nos formatos <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> ou <span class="codeph"> RGBA(R,G,B,A) </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p>Cor de preenchimento da região do mapa de imagem. </p> <p>Especifique esta cor nos formatos <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> ou <span class="codeph"> RGBA(R,G,B,A) </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borda </span> </p> </td> 
   <td colname="col2"> <p> Estilo de borda da região do mapa de imagem. Deve ser especificado como " <span class="codeph"> largura </span> <span class="codeph"> cor sólida </span>", onde <span class="codeph"> largura </span> é expresso em pixels e <span class="codeph"> cor </span> é definido como <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> ou <span class="codeph"> RGBA(R,G,B,A) </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - configurar uma região de mapa de imagem transparente com uma borda preta de um pixel:

```
.s7carouselviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```
