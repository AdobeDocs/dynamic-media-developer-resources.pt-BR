---
description: Propriedades do catálogo de imagens. Retorna atributos comuns do catálogo de imagem especificado no caminho da solicitação.
solution: Experience Manager
title: catalogprops
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---


# catalogprops{#catalogprops}

Propriedades do catálogo de imagens. Retorna atributos comuns do catálogo de imagem especificado no caminho da solicitação.

`req=catalogprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_D1D9183C08834005B482B103CEF2EDA9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Identificador de solicitação exclusivo. </p></td> 
 </tr> 
</table>

Para recuperar as propriedades padrão do catálogo ( [!DNL default.ini]), omita a ID do catálogo. A resposta HTTP pode ser armazenada em cache com o TTL baseado em `attribute::NonImgExpiration`.

As solicitações que oferecem suporte ao formato de resposta JSONP permitem especificar o nome do manipulador de retorno de chamada JS usando a sintaxe estendida do parâmetro `req=`:

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
   <td> <p> <span class="codeph"> catalog.bkgColor</span> </p> </td> 
   <td> <p> hexadecimal </p> </td> 
   <td> <p> <span class="codeph"> atributo::BkgColor</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::defaultExt</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph"> atributo::DefaultExt</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultPix</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> atributo::DefaultPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultThumbPix</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> atributo::DefaultThumbPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.expiration</span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> <span class="codeph"> atributo::Expiration</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultExpiration</span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> <span class="codeph"> atributo::DefaultExpiration</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.nonImgExpiration</span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> <span class="codeph"> atributo::NonImgExpiration</span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog.fileTime</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph"> atributo::LastModified</span> ou, se não estiver presente, a hora da última modificação do  <span class="varname"> catálogo</span><span class="filepath"> .</span> inifile </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.jpegQuality</span> </p> </td> 
   <td> <p> int,bool </p> </td> 
   <td> <p> <span class="codeph"> atributo::JpegQuality</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.maxPix</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> atributo::MaxPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.printResolution</span> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> <span class="codeph"> atributo::PrintResolution</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.publishInfo</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph"> atributo::PublishInfo</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.resMode</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> atributo::ResMode</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.resolution</span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> <span class="codeph"> atributo::Resolution</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbBkgColor</span> </p> </td> 
   <td> <p> hexadecimal </p> </td> 
   <td> <p> <span class="codeph"> atributo::ThumbBkgColor</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbHorizAlign</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> atributo::ThumbHorizAlign</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbRes</span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> <span class="codeph"> atributo::ThumbRes</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbType</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> atributo::ThumbType</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbVertAlign</span> </p> </td> 
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

