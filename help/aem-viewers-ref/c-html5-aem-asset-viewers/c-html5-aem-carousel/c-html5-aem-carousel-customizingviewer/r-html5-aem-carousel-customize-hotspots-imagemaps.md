---
description: O visualizador exibe ícones de pontos de acesso sobre a exibição principal em lugares onde os pontos de acesso foram originalmente criados no Dynamic Media do AEM Assets - sob demanda.
seo-description: O visualizador exibe ícones de pontos de acesso sobre a exibição principal em lugares onde os pontos de acesso foram originalmente criados no Dynamic Media do AEM Assets - sob demanda.
seo-title: Pontos de conexão e mapas de imagem
solution: Experience Manager
title: Pontos de conexão e mapas de imagem
uuid: de7f4dc7-1a55-49d5-a712-7f178cc49068
feature: Dynamic Media Classic,Visualizadores,SDK/API,Banners em carrossel
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---


# Pontos de acesso e mapas de imagem{#hotspots-and-image-maps}

O visualizador exibe ícones de pontos de acesso sobre a exibição principal em lugares onde os pontos de acesso foram originalmente criados no Dynamic Media do AEM Assets - sob demanda.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área principal do visualizador**

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
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo  </span> </p> </td> 
   <td colname="col2"> <p>Arte do ícone de ponto de acesso. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p>Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Scripts CSS </a>. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> fundo  </span> </p> </td> 
   <td colname="col2"> <p>Cor de preenchimento da região do mapa de imagem. </p> <p>Especifique essa cor nos formatos <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> ou <span class="codeph"> RGBA(R,G,B,A) </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p>Cor de preenchimento da região do mapa de imagem. </p> <p>Especifique essa cor nos formatos <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> ou <span class="codeph"> RGBA(R,G,B,A) </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p> Estilo da borda da região do mapa de imagem. Deve ser especificado como " <span class="codeph"> largura </span> <span class="codeph"> cor sólida </span>", onde <span class="codeph"> largura </span> é expressa em pixels e <span class="codeph"> cor </span> é definida como <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) &lt;a1 1/&gt; ou <span class="codeph"> RGBA(R,G,B,A) </span>.</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - configure uma região de mapa de imagem transparente com uma borda preta de um pixel:

```
.s7carouselviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

