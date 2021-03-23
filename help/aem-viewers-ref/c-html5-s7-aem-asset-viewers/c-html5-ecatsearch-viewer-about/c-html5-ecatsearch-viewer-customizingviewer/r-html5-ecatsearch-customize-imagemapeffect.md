---
description: Dependendo do valor do parâmetro de modo, o visualizador exibe ícones de mapa de imagem sobre a exibição principal nos locais em que os mapas são originalmente criados no Dynamic Media Classic ou renderiza regiões exatas que correspondem à forma dos mapas de imagem originais.
solution: Experience Manager
title: Efeito do mapa de imagem
feature: Dynamic Media Classic,Visualizadores,SDK/API,Pesquisa de catálogo eletrônico
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---


# Efeito do mapa de imagem{#image-map-effect}

Dependendo do valor do parâmetro de modo, o visualizador exibe ícones de mapa de imagem sobre a exibição principal nos locais em que os mapas são originalmente criados no Dynamic Media Classic ou renderiza regiões exatas que correspondem à forma dos mapas de imagem originais.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área principal do visualizador**

A aparência do ícone do mapa de imagem é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>A classe CSS `s7mapoverlay` usada para criar estilo de ícones de mapa de imagem no passado agora está obsoleta; em vez disso, use `s7icon`.

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
   <td colname="col2"> <p>Arte do ícone do mapa de imagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largura do ícone do mapa de imagem em pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do ícone do mapa de imagem em pixels. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>O ícone do mapa de imagem é compatível com o seletor de atributos `state`, que pode ser usado para aplicar capas diferentes aos estados de ícones de `default` e `active`.

Exemplo - configure um ícone de mapa de imagem de 28 x 28 pixels que exibe uma imagem diferente para cada um dos dois estados de ícone diferentes.

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon { 
 height: 28px; 
 width: 28px;  
 background-image: url(images/v2/ImageMapEffect_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon[state="default"] { 
 opacity: 0.5; 
} 
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon[state="active"] { 
opacity: 1; 
}
```

Consulte também [Suporte ao mapa de imagem](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a).

A aparência da região do mapa de imagem é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region
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
   <td colname="col1"> <p> <span class="codeph"> fundo  </span> </p> </td> 
   <td colname="col2"> <p> Cor de preenchimento da região do mapa de imagem. </p> <p>Especificado no formato #RRGGBB, RGB(R,G,B) ou RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p> Cor de preenchimento da região do mapa de imagem. </p> <p>Especificado no formato #RRGGBB, RGB(R,G,B) ou RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p> Estilo da borda da região do mapa de imagem. </p> <p>Especificado como <span class="codeph"> <span class="varname"> largura </span> sólida <span class="varname"> cor </span> </span>, onde <span class="codeph"> <span class="varname"> largura </span> </span> é expressa em pixels e <span class="codeph"> <span class="varname"> cor </span> </span> é definido #RRGGBB, RGB(R,G,B) ou RGBA(R,G,B,A). </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - configure uma região do mapa de imagem transparente com `1` pixel de borda preta :

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

