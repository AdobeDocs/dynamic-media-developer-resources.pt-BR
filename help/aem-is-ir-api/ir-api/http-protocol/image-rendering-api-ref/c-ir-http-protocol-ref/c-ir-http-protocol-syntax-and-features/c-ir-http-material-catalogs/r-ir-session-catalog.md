---
description: O catálogo de sessão é o catálogo de materiais que fornece atributos de sessão para a solicitação, bem como um valor catId padrão para todos os comandos src=, vignette= e icc=.
seo-description: O catálogo de sessão é o catálogo de materiais que fornece atributos de sessão para a solicitação, bem como um valor catId padrão para todos os comandos src=, vignette= e icc=.
seo-title: Catálogo de sessões
solution: Experience Manager
title: Catálogo de sessões
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 69c0f6cd-dfaf-47bf-bdd9-7abb4e6f7465
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---


# Catálogo de sessões{#session-catalog}

O catálogo de sessão é o catálogo de materiais que fornece atributos de sessão para a solicitação, bem como um valor catId padrão para todos os comandos src=, vignette= e icc=.

O catálogo de sessão é especificado como o primeiro elemento de caminho do caminho de solicitação HTTP (imediatamente após o nome do servidor). Se o primeiro elemento de caminho não corresponder ao atributo::RootId de qualquer catálogo, o catálogo padrão será usado como catálogo de sessão.

O catálogo de sessão fornece os seguintes valores padrão de sessão:

<table id="table_DB5E0DD8E9B440A4964A1326433597C8"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Atributo </p> </th> 
   <th class="entry"> <p>Notas </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::RootPath</span> </p> </td> 
   <td> <p> Caminho raiz para arquivos de dados de material </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::VignettePath</span> </p> </td> 
   <td> <p> Caminho raiz para arquivos de vinheta </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::IccProfileRgb</span> </p> </td> 
   <td> <p> Espaço de cor de trabalho padrão se uma vinheta não incorporar um perfil ICC </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::RootUrl</span> </p> </td> 
   <td> <p> URL raiz para caminhos de arquivos HTTP relativos nos comandos <span class="codeph"> src=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::ShowOverlapObjs</span> </p> </td> 
   <td> <p> Estado inicial de mostrar/ocultar para objetos sobrepostos </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::Expiração</span> </p> </td> 
   <td> <p> Valor de tempo de vida da imagem de resposta para o servidor proxy e caches do navegador </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::MaxPix</span> </p> </td> 
   <td> <p> A largura e a altura máximas permitidas da imagem de resposta </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::DefaultPix</span> </p> </td> 
   <td> <p> Valores padrão para <span class="codeph"> wid=</span> e <span class="codeph"> hei=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::Format</span> </p> </td> 
   <td> <p> Valor padrão para <span class="codeph"> fmt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::JpegQuality</span> </p> </td> 
   <td> <p> Valor padrão para <span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::TiffEncoding</span> </p> </td> 
   <td> <p> Tipo de compactação para saída de imagem TIFF </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::Nitidez</span> </p> </td> 
   <td> <p> Valor padrão para <span class="codeph"> nitidez=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::OnFailSel</span> </p> </td> 
   <td> <p> Especifica o comportamento quando um comando <span class="codeph"> sel=</span> falha </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::OnFailObj</span> </p> </td> 
   <td> <p> Especifica o comportamento quando um comando <span class="codeph"> obj=</span> falha </p> </td> 
  </tr> 
 </tbody> 
</table>

