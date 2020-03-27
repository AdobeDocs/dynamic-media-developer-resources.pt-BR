---
description: Dependendo do valor do parâmetro de modo, o visualizador exibe ícones de mapa de imagem sobre a visualização principal nos locais em que os mapas são criados originalmente no Scene7 Publishing System ou renderiza regiões exatas que correspondem à forma dos mapas de imagem originais.
seo-description: Dependendo do valor do parâmetro de modo, o visualizador exibe ícones de mapa de imagem sobre a visualização principal nos locais em que os mapas são criados originalmente no Scene7 Publishing System ou renderiza regiões exatas que correspondem à forma dos mapas de imagem originais.
seo-title: Efeito Mapa de imagem
solution: Experience Manager
title: Efeito Mapa de imagem
topic: Dynamic media
uuid: 193d2f4e-77a2-4741-bf36-90ca31c600c6
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Efeito Mapa de imagem{#image-map-effect}

Dependendo do valor do parâmetro de modo, o visualizador exibe ícones de mapa de imagem sobre a visualização principal nos locais em que os mapas são criados originalmente no Scene7 Publishing System ou renderiza regiões exatas que correspondem à forma dos mapas de imagem originais.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades de CSS da área do visualizador principal**

A aparência do ícone do mapa de imagem é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>A classe `s7mapoverlay` CSS usada para estilizar ícones de mapa de imagem no passado agora está obsoleta; use `s7icon` em vez disso.

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Arte-final do ícone do mapa de imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da sprite de arte, se os sprites CSS forem usados. </p> <p>Consulte também Sprites <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largura do ícone do mapa de imagens em pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do ícone do mapa de imagens em pixels. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>O ícone do mapa de imagens suporta o seletor de `state` atributos, que você pode usar para aplicar diferentes capas aos estados de ícones de `default` e `active`.

Exemplo - configure um ícone de mapa de imagem de 28 x 28 pixels que exiba uma imagem diferente para cada um dos dois estados de ícone diferentes.

```
.s7ecatalogviewer .s7imagemapeffect .s7icon { 
 height: 28px; 
 width: 28px;  
 background-image: url(images/v2/ImageMapEffect_dark_up.png); 
} 
.s7ecatalogviewer .s7imagemapeffect .s7icon[state="default"] { 
 opacity: 0.5; 
} 
.s7ecatalogviewer .s7imagemapeffect .s7icon[state="active"] { 
opacity: 1; 
}
```

Consulte também Suporte [ao mapa de](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a)imagens.

A aparência da região do mapa de imagem é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7imagemapeffect .s7region
```

<table id="table_1FF98CE842604AAABD838FF528CDC4EF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fundo </span> </p> </td> 
   <td colname="col2"> <p> Cor de preenchimento da região do mapa de imagem. </p> <p>Especificado no formato #RRGGBB, RGB(R,G,B) ou RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p> Cor de preenchimento da região do mapa de imagem. </p> <p>Especificado no formato #RRGGBB, RGB(R,G,B) ou RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fronteira </span> </p> </td> 
   <td colname="col2"> <p> Estilo da borda da região do mapa de imagens. </p> <p>Especificada como <span class="codeph"> largura <span class="varname"> cor sólida </span> <span class="varname"> , onde </span> largura é expressa em pixels </span>e  cor é definida como # <span class="codeph"> <span class="varname"> </span> </span> <span class="codeph"> <span class="varname"> </span> </span> RRGGBB, RGB(R,G,B) ou RGBA(R,G,B,A). </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - configure uma região transparente do mapa de imagem com borda preta de `1` pixel :

```
.s7ecatalogviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

