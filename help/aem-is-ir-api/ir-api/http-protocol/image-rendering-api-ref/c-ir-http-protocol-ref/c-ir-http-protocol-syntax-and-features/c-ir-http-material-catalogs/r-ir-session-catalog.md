---
title: Catálogo da sessão
description: O catálogo de sessões é o catálogo de materiais que fornece atributos de sessão para a solicitação e um valor catId padrão para todos os comandos src=, vignette= e icc=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36e0571e-7451-423f-a1df-540680381902
TQID: 'https://experienceleague.adobe.com/--3F69i8XdliFxf5IhMPbUThRzMNyIDjtW4-Y-SBCFE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 235
ht-degree: 0%

---

# Catálogo da sessão{#session-catalog}

O catálogo de sessões é o catálogo de materiais que fornece atributos de sessão para a solicitação e um valor de catId padrão para todos os comandos `src=`, `vignette=` e `icc=`.

O catálogo de sessões é especificado como o primeiro elemento de caminho do caminho de solicitação HTTP (imediatamente após o nome do servidor). Se o primeiro elemento de caminho não corresponder a attribute::RootId de qualquer catálogo, o catálogo padrão será usado como um catálogo de sessão.

O catálogo de sessões fornece os seguintes valores padrão de sessão:

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
   <td> <p> URL raiz para caminhos de arquivos HTTP relativos em comandos <span class="codeph"> src=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::ShowOverlapObjs</span> </p> </td> 
   <td> <p> Estado inicial de exibição/ocultação para objetos sobrepostos </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::Expiration</span> </p> </td> 
   <td> <p> Valor de vida útil da imagem de resposta para o servidor proxy e os caches do navegador </p> </td> 
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
   <td> <p> Tipo de compactação para saída de imagem do TIFF </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::nitidez</span> </p> </td> 
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

