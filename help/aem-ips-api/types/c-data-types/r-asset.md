---
description: Um objeto ou container na hierarquia de pastas.
seo-description: Um objeto ou container na hierarquia de pastas.
seo-title: Ativo
solution: Experience Manager
title: Ativo
topic: Scene7 Image Production System API
uuid: 758ac593-98d8-4366-a723-a06435c7fd3c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Ativo{#asset}

Um objeto ou container na hierarquia de pastas.

Sintaxe

## Parâmetros {#section-0f2abb29deaf4d73bbbd0a5a2dc9ca3b}

<table id="table_C58EF9963CB34179A9D6C9F0F6FF24F2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> acoInfo</span></span> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> animatedGifInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AnimatedGifInfo</span> </td> 
   <td colname="col3"> Detalhes sobre um arquivo GIF animado. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Identificador de ativos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSetInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> gabineteInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:CabinetInfo</span> </td> 
   <td colname="col3"> Propriedades de um tipo de ativo de gabinete. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> criado</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Data e hora em que o ativo foi carregado. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createUser</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Endereço de email do usuário que criou o ativo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> cssInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:CssInfo</span> </td> 
   <td colname="col3"> Detalhes sobre um arquivo CSS. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> cuePointInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excelInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fileName</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Retorna o nome do arquivo virtual. O caminho completo do arquivo virtual é <span class="codeph"> folder</span>+<span class="codeph"> fileName</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> flashInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pasta</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Pasta que contém um ativo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Lidar com a pasta pai do ativo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fontInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:fontInfo</span> </td> 
   <td colname="col3"> Propriedades de um ativo de fonte. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> iccProfileInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:IccProfileInfo</span> </td> 
   <td colname="col3"> Propriedades de um ativo de perfil ICC. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> illustratorInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ImageInfo</span> </td> 
   <td colname="col3"> Propriedades de um ativo de imagem. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ipsImageUrl</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> URL relativo que representa uma visualização em miniatura do ativo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> javascriptInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:JavascriptInfo</span> </td> 
   <td colname="col3"> Detalhes sobre um arquivo JavaScript. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastModified</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Data e hora em que o ativo foi modificado pela última vez. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastModifyUser</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Endereço de email do usuário que modificou o ativo pela última vez. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> layerViewInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:LayerViewInfo</span> </td> 
   <td colname="col3"> Propriedades de um ativo de visualização de camada. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> maskInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> masterVideoInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:MetadataArray</span> </td> 
   <td colname="col3"> Matriz de valores de metadados associados ao ativo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nome</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nome do ativo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfSettingsInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:PdfSettingsInfo</span> </td> 
   <td colname="col3"> Propriedades de um ativo de configurações de PDF. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> permissões</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> PowerPointInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> premiereExpressInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projetos</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Lista de nomes de projetos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> psdInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> Define um sinalizador para indicar se um ativo deve ser publicado ou não. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> renderSceneInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:RenderSceneInfo</span> </td> 
   <td colname="col3"> Propriedades de um ativo de cena de renderização. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> rtfInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> subtipo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Subtipo de ativo genérico que suporta valores de subtipo (por exemplo, <span class="codeph"> AssetSet</span>). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> svgInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:SvgInfo</span> </td> 
   <td colname="col3"> Propriedades de um ativo SVG. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> swcInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:SwcInfo</span> </td> 
   <td colname="col3"> Propriedades de um ativo SWC. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> templateInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:TemplateInfo</span> </td> 
   <td colname="col3"> Propriedades de um ativo de modelo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Indica se um ativo está na lixeira ou ao vivo (consulte "Estado da lixeira" para obter valores). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tipo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Tipo de ativo. Consulte <a href="../../string-constants/c-string-constants/r-asset-types.md#reference-2fe75d230663419d88632d30f1144a10" format="dita" scope="local"> Tipos</a> de ativos para obter valores. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoCaptionInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:VideoCaptionInfo</span> </td> 
   <td colname="col3"> <p>Propriedades de um ativo de legenda de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> <p>Propriedades de um ativo de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> viewerPresetInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ViewerPresetInfo</span> </td> 
   <td colname="col3"> Propriedades de um ativo predefinido do visualizador. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> viewerSwfInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ViewerSwfInfo</span> </td> 
   <td colname="col3"> Propriedades de um ativo do visualizador SWf. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> vinhetaInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:VignetteInfo</span> </td> 
   <td colname="col3"> Propriedades de um ativo de vinheta. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> watermarkInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:WatermarkInfo</span> </td> 
   <td colname="col3"> Propriedades de um ativo de marca d'água. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> windowCoveringInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:WindowCoveringInfo</span> </td> 
   <td colname="col3"> Propriedades de uma janela que cobre o ativo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> wordInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xmlInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:XmlInfo</span> </td> 
   <td colname="col3"> Propriedades de um ativo XML. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xslInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:XslInfo</span> </td> 
   <td colname="col3"> Propriedades de um ativo XSL. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> zipInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

