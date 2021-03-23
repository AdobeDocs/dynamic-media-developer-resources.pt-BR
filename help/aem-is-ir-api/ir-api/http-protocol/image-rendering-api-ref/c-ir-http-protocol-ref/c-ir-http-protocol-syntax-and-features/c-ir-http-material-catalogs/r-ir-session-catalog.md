---
description: O catálogo de sessão é o catálogo de material que fornece atributos de sessão para a solicitação, bem como um valor catId padrão para todos os comandos src=, vinheta= e icc=.
seo-description: O catálogo de sessão é o catálogo de material que fornece atributos de sessão para a solicitação, bem como um valor catId padrão para todos os comandos src=, vinheta= e icc=.
seo-title: Catálogo de sessão
solution: Experience Manager
title: Catálogo de sessão
uuid: 69c0f6cd-dfaf-47bf-bdd9-7abb4e6f7465
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---


# Catálogo de sessão{#session-catalog}

O catálogo de sessão é o catálogo de material que fornece atributos de sessão para a solicitação, bem como um valor catId padrão para todos os comandos src=, vinheta= e icc=.

O catálogo de sessão é especificado como o primeiro elemento de caminho do caminho de solicitação HTTP (imediatamente após o nome do servidor). Se o primeiro elemento de caminho não corresponder ao atributo::RootId de qualquer catálogo, o catálogo padrão será usado como um catálogo de sessão.

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
   <td> <p> Espaço de cores de trabalho padrão se uma vinheta não incorporar um perfil ICC </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::RootUrl</span> </p> </td> 
   <td> <p> URL raiz para caminhos de arquivo HTTP relativos nos comandos <span class="codeph"> src=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::ShowOvercomandoObjs</span> </p> </td> 
   <td> <p> Estado inicial de mostrar/ocultar para objetos de sobreposição </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::Expiration</span> </p> </td> 
   <td> <p> Valor do tempo de vida da imagem de resposta para caches do servidor proxy e do navegador </p> </td> 
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
   <td> <p> <span class="codeph"> atributo::Formato</span> </p> </td> 
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

