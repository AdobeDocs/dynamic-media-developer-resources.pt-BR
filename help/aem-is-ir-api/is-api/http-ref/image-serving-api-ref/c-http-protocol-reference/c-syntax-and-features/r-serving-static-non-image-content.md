---
description: Veiculação de conteúdo estático (não relacionado à imagem)
solution: Experience Manager
title: Veiculação de conteúdo estático (não relacionado à imagem)
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e2c79bdc-5d70-46d9-85f4-ffebd7621944
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Veiculação de conteúdo estático (não relacionado à imagem){#serving-static-non-image-content}

O Servidor de Imagens fornece um mecanismo para gerenciar conteúdos que não sejam de imagens em catálogos e distribuí-los por meio de um `context /is/content` separado. O mecanismo permite configurar o TTL para cada item separadamente.

## Sintaxe básica {#section-a986baaca8644d04bcd0ddf781ae916e}

<table id="simpletable_4A6249F0C40747339524323EB0831CE4"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> solicitação </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> http:// <span class="varname"> servidor </span>/is/content[/ <span class="varname"> catálogo </span>/ <span class="varname"> item </span>[? <span class="varname"> modificadores </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> servidor </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> endereço_do_servidor </span>[: <span class="varname"> porta </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> catálogo </span> </span> </p> </td> 
  <td class="stentry"> <p>Identificador do catálogo. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> item </span> </span> </p> </td> 
  <td class="stentry"> <p>ID do item de conteúdo estático. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> modificadores </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> comando </span>*[&amp; <span class="varname"> comando </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> comando </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span>= <span class="varname"> valor </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span> </span> </p> </td> 
  <td class="stentry"> <p>Um dos nomes de comando compatíveis. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> valor </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor do comando. </p> </td> 
 </tr> 
</table>

## Visão geral do comando {#section-61657a0141914053ab12038ad7e91500}

O Servidor de imagens é compatível com os seguintes comandos em /is/content:

<table id="simpletable_1D96BA1AB5394B3C9B91D46617AFC0FA"> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" type="reference" format="dita" scope="local"> tipo </a> </td> 
  <td class="stentry"> <p>Filtro de tipo de conteúdo. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req </a> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>, <span class="codeph"> req=props </span> e <span class="codeph"> req=existe somente </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" type="reference" format="dita" scope="local"> cache </a> </td> 
  <td class="stentry"> <p>Permite desabilitar o cache do lado do cliente. </p> </td> 
 </tr> 
</table>

## Catálogos de conteúdo estático {#section-b2b8f4860fe84e528493ed704c7c5141}

Os catálogos de conteúdo estático são semelhantes aos catálogos de imagem, mas oferecem suporte a menos campos de dados:

<table id="table_3B111EC3AA1044FB9B659FD54BADDC39"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Atributo/Dados</b> </th> 
   <th class="entry"> <b> Notas</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::Id </span> </p> </td> 
   <td> <p> O identificador de registro de catálogo para este item de conteúdo estático </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::Caminho </span> </p> </td> 
   <td> <p> O caminho de arquivo para este item de conteúdo </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::Expiração </span> </p> </td> 
   <td> <p> O TTL deste item de conteúdo; attribute::Expiration é usado se não especificado ou se estiver vazio </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::Carimbo de data/hora </span> </p> </td> 
   <td> <p> Carimbo de data/hora de modificação de arquivo; necessário quando a validação baseada em catálogo está habilitada com o atributo::CacheValidationPolicy </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::UserData </span> </p> </td> 
   <td> <p> Metadados opcionais associados a este item de conteúdo estático; disponíveis para o cliente com req=userdata </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catálogo::UserType </span> </p> </td> 
   <td> <p> Tipo de dados opcional; pode ser usado para filtrar solicitações de conteúdo estático com o comando type= </p> </td> 
  </tr> 
 </tbody> 
</table>

## Filtragem de conteúdo estático {#section-896c37cf68bc446eb0766fb378898262}

Esse mecanismo pode ajudar a garantir que os clientes recebam apenas o conteúdo apropriado para suas necessidades. Supondo que o conteúdo estático esteja marcado com `catalog::UserType` valores apropriados, o cliente poderá adicionar o comando `type=` à solicitação. O Servidor de imagens compara o valor fornecido com o comando `type=` ao valor de `catalog::UserType` e, em caso de incompatibilidade, retorna um erro em vez de conteúdo potencialmente inadequado.

## Consulte também {#section-91c7b686aacf4d3ca974f35a3fe3d6ec}

[tipo=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Referência do Catálogo de Imagens](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
