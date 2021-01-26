---
description: Propriedades do catálogo de imagens. Retorna atributos comuns do catálogo de imagens especificado no caminho da solicitação.
seo-description: Propriedades do catálogo de imagens. Retorna atributos comuns do catálogo de imagens especificado no caminho da solicitação.
seo-title: catalogprops
solution: Experience Manager
title: catalogprops
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 09252d39-8604-4785-bcdc-ad229a691035
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---


# catalogprops{#catalogprops}

Propriedades do catálogo de imagens. Retorna atributos comuns do catálogo de imagens especificado no caminho da solicitação.

`req=catalogprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_D1D9183C08834005B482B103CEF2EDA9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Identificador de solicitação exclusivo. </p></td> 
 </tr> 
</table>

Omitir a ID do catálogo para recuperar as propriedades padrão do catálogo ( [!DNL default.ini]). A resposta HTTP pode ser armazenada em cache com o TTL baseado em `attribute::NonImgExpiration`.

As solicitações compatíveis com o formato de resposta JSONP permitem que você especifique o nome do manipulador de retorno de chamada JS usando a sintaxe estendida do parâmetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` é o nome do manipulador JS presente na resposta JSONP. Somente caracteres a-z, A-Z e 0-9 são permitidos. Opcional. O padrão é `s7jsonResponse`.

Os seguintes valores de propriedade são retornados:

<table id="table_DEC26CBF274945298BA81B5E2E2F331D"> 
 <tbody> 
  <tr> 
   <td> <b> Propriedade</b> </td> 
   <td> <b> Tipo</b> </td> 
   <td> <b> Atributo de catálogo correspondente</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Catalog.bkgColor</span> </p> </td> 
   <td> <p> hexadecimal </p> </td> 
   <td> <p> <span class="codeph"> atributo::BkgColor</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::defaultExt</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph"> atributo::DefaultExt</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Catalog.defaultPix</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> atributo::DefaultPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Catalog.defaultThumbPix</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> atributo::DefaultThumbPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Catalog.expiration</span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> <span class="codeph"> atributo::Expiração</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Catalog.defaultExpiration</span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> <span class="codeph"> atributo::DefaultExpiration</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Catalog.nonImgExpiration</span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> <span class="codeph"> atributo::NonImgExpiration</span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> Catalog.fileTime</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph"> atributo::LastModified</span> ou, se não estiver presente, a última hora modificada de  <span class="varname"> Catalog</span><span class="filepath"> .</span> inifile </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Catalog.jpegQuality</span> </p> </td> 
   <td> <p> int,bool </p> </td> 
   <td> <p> <span class="codeph"> atributo::JpegQuality</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Catalog.maxPix</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> atributo::MaxPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Catalog.printResolution</span> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> <span class="codeph"> atributo::PrintResolution</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Catalog.publishInfo</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph"> atributo::PublishInfo</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Catalog.resMode</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> atributo::ResMode</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Catalog.resolution</span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> <span class="codeph"> atributo::Resolution</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Catalog.thumbBkgColor</span> </p> </td> 
   <td> <p> hexadecimal </p> </td> 
   <td> <p> <span class="codeph"> atributo::ThumbBkgColor</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Catalog.thumbHorizAlign</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> atributo::ThumbHorizAlign</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Catalog.thumbRes</span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> <span class="codeph"> atributo::ThumbRes</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Catalog.thumbType</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> atributo::ThumbType</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Catalog.thumbVertAlign</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> atributo::ThumbVertAlign</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo:marca d'água</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph"> atributo::Marca d'água</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

