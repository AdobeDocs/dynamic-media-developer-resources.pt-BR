---
description: Parâmetro comum a todos os visualizadores.
solution: Experience Manager
title: ativo
feature: Dynamic Media Classic,Visualizadores,SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 0%

---


# asset{#asset}

Parâmetro comum a todos os visualizadores.

` asset= *`assetId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> assetId  </span> </span> </p> </td> 
   <td colname="col2"> <p> A ID do ativo do vídeo único ou do Conjunto de vídeos adaptáveis. </p> </td> 
  </tr> 
 </tbody> 
</table>

Essa propriedade é necessária, a menos que o parâmetro `video` seja usado. Consulte [Suporte a vídeo externo](../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3) em Vídeo ou [Suporte a vídeo externo](../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) em Vídeo360.

ou

` asset= *`imagem`*`

<table id="table_67E18F42E97C4AAAB0A2F67B7924765D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imagem  </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica uma única imagem ou um conjunto de carrossel. Aplique codificação HTTP dupla a qualquer caractere não seguro que exista no nome da imagem ou no nome do conjunto de carrossel. </p> </td> 
  </tr> 
 </tbody> 
</table>

ou

` asset= *``* | *``* | *``* | *``* [%3F *`imageimageListWithModifiersmultiDimensionalSpinSetmodifiers`*]`

<table id="table_A2A0ACD942E942BC99AF0DC80FB1C670"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imagem  </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica uma única imagem. Aplique codificação HTTP dupla a qualquer caractere não seguro que exista no nome da imagem. </p> <p>Ou especifica uma referência para um conjunto de imagens. O visualizador recupera conjuntos de imagens do servidor, usando a solicitação <span class="codeph"> req=set IS </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageList  </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica um conjunto de imagens explícito, que consiste em uma sequência ordenada de itens ou quadros, separados por vírgulas. </p> <p> <p>Observação:  Esse recurso é compatível com o Adobe Dynamic Media Classic; não é compatível com o Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageListWithModifiers  </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica um conjunto de imagens explícito em que cada quadro tem seus próprios modificadores de Exibição de imagem. Nesse caso, a lista de quadros é encapsulada entre parênteses. Certifique-se de aplicar a codificação HTTP dupla a qualquer vírgula que esteja presente no modificador de Exibição de imagem específico do quadro. </p> <p> <p>Observação:  Esse recurso é compatível com o Adobe Dynamic Media Classic; não é compatível com o Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> multiDimensionalSpinSet  </span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica um conjunto de rotação multidimensional explícito usando a seguinte sintaxe: </p> <p> <span class="codeph"> ((  <span class="varname"> horizontalSpinSet  </span>)[,(  <span class="varname"> horizontalSpinSet  </span>)])  </span> </p> <p> onde <span class="codeph"> <span class="varname"> horizontalSpinSet </span> </span> é uma lista de quadros separada por vírgulas para um determinado eixo horizontal. Todos os <span class="codeph"> <span class="varname"> horizontalSpinSet </span> </span> devem ter o mesmo número de quadros. </p> <p> <p>Observação:  Esse recurso é compatível com o Adobe Dynamic Media Classic; não é compatível com o Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> modificadores  </span> </span> </p> </td> 
   <td colname="col2"> <p> Comandos do Image Serving; Os separadores <span class="codeph"> &amp; </span> e <span class="codeph"> = </span> devem ser codificados por HTTP como <span class="codeph"> %26 </span> e <span class="codeph"> %3D </span>, respectivamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

ou

` asset=( *``* | ( *``*; *``* | *``*; *``* | *``*; *``*); *``*;( *``*; *``* | *``*; *``* | *``*; *``*); *``*;] [%3F *`mediaSetvideoswatchIdimageswatchIdsetIdswatchIdIDvideoswatchIdimageswatchIdsetIdswatchIdIDmodifiers`*]`

<table id="table_D31C8507C02A4452A79DEDDEC62EF2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> mediaSet  </span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica uma referência a um conjunto de mídia. O visualizador recupera conjuntos de mídia do servidor, usando req=set IS request. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> vídeo  </span> </span> </p> </td> 
   <td colname="col2"> <p> Vídeo único ou Conjunto de vídeos adaptáveis. </p> <p> <p>Observação:  Esse recurso é compatível com o Adobe Dynamic Media Classic; não é compatível com o Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imagem  </span> </span> </p> </td> 
   <td colname="col2"> <p> Imagem única. </p> <p> <p>Observação:  Esse recurso é compatível com o Adobe Dynamic Media Classic; não é compatível com o Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> setId  </span> </span> </p> </td> 
   <td colname="col2"> <p> Conjunto de amostras. </p> <p> <p>Observação:  Esse recurso é compatível com o Adobe Dynamic Media Classic; não é compatível com o Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> swatchId  </span> </span> </p> </td> 
   <td colname="col2"> <p>Amostra de imagem. </p> <p> <p>Observação:  Esse recurso é compatível com o Adobe Dynamic Media Classic; não é compatível com o Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ID  </span> </span> </p> </td> 
   <td colname="col2"> <p> O identificador de tipo de item Conjunto de mídia pode ser um dos seguintes: </p> <p> 
     <ul id="ul_3100F9356628498DA820C07F6F69CC9B"> 
      <li id="li_51B649A539F14510873CFDA85A6AA714"> <p> <span class="codeph"> advanced_image  </span> </p> <p>Para imagem única. </p> </li> 
      <li id="li_7E764D67294647C1A828F949E5ED1908"> <p> <span class="codeph"> advanced_swatchset  </span> </p> <p>Para conjunto de amostras aninhado. </p> </li> 
      <li id="li_C942CED779B54110BCDC74188995FD5B"> <p> <span class="codeph"> rotação  </span> </p> <p>Para conjunto de rotação. </p> </li> 
      <li id="li_6EA5C54F078D4B24B44F1588BF083842"> <p> <span class="codeph"> vídeo  </span> </p> <p>Para vídeo único. </p> </li> 
      <li id="li_8110FA7E0CAB4681A2D8C15F2A656E69"> <p> <span class="codeph"> video_set  </span> </p> <p>Para Conjuntos De Vídeos Adaptáveis. </p> </li> 
     </ul> </p> <p> <p>Observação:  Esse recurso é compatível com o Adobe Dynamic Media Classic; não é compatível com o Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> modificadores  </span> </span> </p> </td> 
   <td colname="col2"> <p> Comandos do Image Serving; Os separadores <span class="codeph"> &amp; </span> e <span class="codeph"> = </span> devem ser codificados por HTTP como <span class="codeph"> %26 </span> e <span class="codeph"> %3D </span>, respectivamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Imagens que usam IR (Renderização de Imagem) ou UGC (Conteúdo Gerado pelo Usuário) não são suportadas por esse visualizador.

## Propriedades {#section-10ee45d637134e0fbcd943c62578cb78}

Obrigatório.

## Padrão {#section-d411e450028c460392cb8508f8ccc5d9}

Nenhum.

## Exemplos {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

Referência de ativo único:

```
asset=Scene7SharedAssets/Backpack_B
```

ou

```
asset=/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg
```

ou

```
asset=/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4
```

ou

```
asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner
```

ou

```
asset=Viewers/space_station_360-AVS
```

Referência única a um conjunto de imagens definido em um catálogo:

```
asset=Viewers/Pluralist
```

Conjunto de imagens explícito:

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C
```

Conjunto de imagens explícito com modificadores de Exibição de imagens específicos de quadro:

```
asset=(Scene7SharedAssets/Backpack_B%3Fop_colorize%3D255%252C0%252C0,Scene7SharedAssets/Backpack_B%3Fop_colorize%3D0x00ff00)
```

Referência única para um conjunto de rotação que é definido em um catálogo:

```
asset=Scene7SharedAssets/SpinSet-Sample
```

Conjunto de rotação explícito:

```
asset=Scene7SharedAssets/Frame-1,Scene7SharedAssets/Frame-2,Scene7SharedAssets/Frame-3,Scene7SharedAssets/Frame-4,Scene7SharedAssets/Frame-5,Scene7SharedAssets/Frame-6,Scene7SharedAssets/Frame-7,Scene7SharedAssets/Frame-8
```

Conjunto de rotação multidimensional explícito:

```
asset=((Scene7SharedAssets/ring1-25,Scene7SharedAssets/ring1-26,Scene7SharedAssets/ring1-27,Scene7SharedAssets/ring1-28,Scene7SharedAssets/ring1-29,Scene7SharedAssets/ring1-30,Scene7SharedAssets/ring1-31,Scene7SharedAssets/ring1-32,Scene7SharedAssets/ring1-33,Scene7SharedAssets/ring1-34,Scene7SharedAssets/ring1-35,Scene7SharedAssets/ring1-36),(Scene7SharedAssets/ring1-13,Scene7SharedAssets/ring1-14,Scene7SharedAssets/ring1-15,Scene7SharedAssets/ring1-16,Scene7SharedAssets/ring1-17,Scene7SharedAssets/ring1-18,Scene7SharedAssets/ring1-19,Scene7SharedAssets/ring1-20,Scene7SharedAssets/ring1-21,Scene7SharedAssets/ring1-22,Scene7SharedAssets/ring1-23,Scene7SharedAssets/ring1-24),(Scene7SharedAssets/ring1-01,Scene7SharedAssets/ring1-02,Scene7SharedAssets/ring1-03,Scene7SharedAssets/ring1-04,Scene7SharedAssets/ring1-05,Scene7SharedAssets/ring1-06,Scene7SharedAssets/ring1-07,Scene7SharedAssets/ring1-08,Scene7SharedAssets/ring1-09,Scene7SharedAssets/ring1-10,Scene7SharedAssets/ring1-11,Scene7SharedAssets/ring1-12))
```

Referência do conjunto de mídia mista única:

```
 asset=Scene7SharedAssets/Mixed_Media_Set_Sample
```

Conjunto de mídias mistas explícito:

```
asset=Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;
```

Modificador de nitidez adicionado a todas as imagens no conjunto:

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C%3Fop_sharpen=%3D1
```

```
asset=Scene7SharedAssets/Mixed_Media_Set_Sample%3Fop_sharpen%3D1
```

```
asset=Viewers/Pluralist%3Fop_sharpen%3D1
```

