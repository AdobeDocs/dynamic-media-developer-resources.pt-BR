---
description: O indicador de zoom está sobreposto na área da visualização principal. Ela é exibida quando a imagem está em um estado de redefinição e também depende do parâmetro de efeito de ícone.
seo-description: O indicador de zoom está sobreposto na área da visualização principal. Ela é exibida quando a imagem está em um estado de redefinição e também depende do parâmetro de efeito de ícone.
seo-title: Efeito Ícone
solution: Experience Manager
title: Efeito Ícone
topic: Dynamic Media
uuid: 9e8c0c6f-2c45-4acb-9acb-5b8494bfc69b
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---


# Efeito de ícone{#icon-effect}

O indicador de zoom está sobreposto na área da visualização principal. Ela é exibida quando a imagem está em um estado de redefinição e também depende do parâmetro de efeito de ícone.

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
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Arte do indicador de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da sprite de arte, se os sprites CSS forem usados. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largura do indicador de zoom em pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do indicador de zoom em pixels. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>O efeito de ícone suporta o seletor de atributos `media-type`, que você pode usar para aplicar efeitos de ícones diferentes em dispositivos diferentes. Em particular, `media-type='standard'` corresponde a sistemas de desktop onde a entrada do mouse é normalmente usada e `media-type='multitouch'` corresponde a dispositivos com entrada de toque.

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

