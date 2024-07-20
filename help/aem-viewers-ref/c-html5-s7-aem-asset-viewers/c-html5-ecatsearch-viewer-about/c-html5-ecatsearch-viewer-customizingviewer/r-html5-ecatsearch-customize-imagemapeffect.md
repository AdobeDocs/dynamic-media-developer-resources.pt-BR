---
title: Efeito do mapa de imagem
description: Dependendo do valor do parâmetro de modo, o visualizador exibe ícones de mapa de imagem sobre a exibição principal em locais onde os mapas são originalmente criados no Dynamic Media Classic ou renderiza regiões exatas que correspondem à forma dos mapas de imagem originais.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 873fc387-1d2a-4d74-b85e-fcbb13b691c5
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---

# Efeito do mapa de imagem{#image-map-effect}

Dependendo do valor do parâmetro de modo, o visualizador exibe ícones de mapa de imagem sobre a exibição principal em locais onde os mapas são originalmente criados no Dynamic Media Classic ou renderiza regiões exatas que correspondem à forma dos mapas de imagem originais.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriedades CSS da área do visualizador principal**

A aparência do ícone do mapa de imagem é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>A classe CSS `s7mapoverlay` usada para estilizar ícones de mapa de imagem no passado agora está obsoleta; use `s7icon` em seu lugar.

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
   <td colname="col2"> <p>Ícone do mapa de imagem arte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do ícone do mapa de imagem em pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do ícone do mapa de imagem em pixels. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>O ícone de mapa de imagem oferece suporte ao seletor de atributos `state`, que você pode usar para aplicar capas diferentes aos estados de ícone de `default` e `active`.

Exemplo - configure um ícone de mapa de imagem de 28 x 28 pixels que exiba uma imagem diferente para cada um dos dois estados de ícone diferentes.

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

Consulte também [Suporte a mapa de imagem](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a).

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
   <td colname="col1"> <p> <span class="codeph"> plano de fundo </span> </p> </td> 
   <td colname="col2"> <p> Cor de preenchimento da região do mapa de imagem. </p> <p>Especificado no formato #RRGGBB, RGB(R,G,B) ou RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p> Cor de preenchimento da região do mapa de imagem. </p> <p>Especificado no formato #RRGGBB, RGB(R,G,B) ou RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borda </span> </p> </td> 
   <td colname="col2"> <p> Estilo de borda da região do mapa de imagem. </p> <p>Especificado como <span class="codeph"> <span class="varname"> largura </span> cor <span class="varname"> sólida </span> </span>, onde <span class="codeph"> <span class="varname"> largura </span> </span> é expresso em pixels e <span class="codeph"> <span class="varname"> cor </span> </span> é definido como #RRGGBB, RGB(R,G,B) ou RGBA(R,G,B,A). </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - configurar uma região de mapa de imagem transparente com borda preta de `1` pixels:

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```
