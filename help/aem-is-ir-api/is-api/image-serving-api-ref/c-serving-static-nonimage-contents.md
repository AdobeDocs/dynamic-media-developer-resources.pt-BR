---
title: Veiculação de conteúdo estático (não imagem)
description: Você pode usar o Servidor de imagens para gerenciar conteúdo não relacionado a imagens em catálogos e disponibilizá-lo por meio de um contexto /is/content separado.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: adc3d972-b02d-40db-992e-acaa06b848ff
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Veiculação de conteúdo estático (não imagem){#serving-static-non-image-contents}

Você pode usar o Servidor de imagens para gerenciar conteúdo não relacionado a imagens em catálogos e disponibilizá-lo por meio de um contexto /is/content separado.

Esse recurso permite configurar o TTL para cada item separadamente.

O Servidor de imagens oferece suporte aos seguintes comandos em [!DNL /is/content]:

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> tipo </a> </p> </td> 
  <td class="stentry"> <p>Filtro de tipo de conteúdo. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> req </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>, <span class="codeph"> req=props </span> e <span class="codeph"> req=existe somente </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> cache </a> </p> </td> 
  <td class="stentry"> <p>Permite desabilitar o cache do lado do cliente. </p> </td> 
 </tr> 
</table>

## Sintaxe básica {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> solicitação </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http:// <span class="varname"> servidor </span>/is/content[/catalog/ <span class="varname"> item </span>][? <span class="varname"> modificadores </span>] </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> servidor </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> endereço_do_servidor </span>[ : <span class="varname"> porta </span>] </span> </p> </td> 
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

## Catálogos de conteúdo estático {#section-91014f17f0d543d7aaf24539b2d7d4b9}

Os catálogos de conteúdo estático são semelhantes aos catálogos de imagem, mas oferecem suporte a menos campos de dados:

<table id="table_71A565DF5EC94913AD35CB13B0C7A27D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Atributo/Dados </p> </th> 
   <th colname="col2" class="entry"> <p>Notas </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catálogo::Id </span> </p> </td> 
   <td colname="col2"> <p>O identificador de registro de catálogo para este item de conteúdo estático. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catálogo::Caminho </span> </p> </td> 
   <td colname="col2"> <p>O caminho de arquivo para este item de conteúdo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catálogo::Expiração </span> </p> </td> 
   <td colname="col2"> <p>O TTL deste item de conteúdo; o atributo <span class="codeph">::Expiration </span> será usado se não for especificado ou se estiver vazio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catálogo::Carimbo de data/hora </span> </p> </td> 
   <td colname="col2"> <p>Carimbo de data/hora de modificação de arquivo; necessário quando a validação baseada em catálogo está habilitada com o atributo <span class="codeph">::CacheValidationPolicy </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catálogo::UserData </span> </p> </td> 
   <td colname="col2"> <p>Metadados opcionais associados a este item de conteúdo estático; disponíveis para o cliente com <span class="codeph"> req=userdata </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catálogo::UserType </span> </p> </td> 
   <td colname="col2"> <p>Tipo de dados opcional; pode ser usado para filtrar solicitações de conteúdo estático com o comando <span class="codeph"> type= </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Filtragem de conteúdo estático {#section-4c41bf41ff994910840c1352683d1f37}

Esse mecanismo pode ajudar a garantir que os clientes recebam apenas o conteúdo apropriado para suas necessidades. Supondo que o conteúdo estático esteja marcado com os `catalog::UserType` valores apropriados, o cliente pode adicionar o comando `type=` à solicitação. O Servidor de imagens compara o valor fornecido com o comando `type=` ao valor de `catalog::UserType` e, se houver uma incompatibilidade, retorna um erro em vez de conteúdo potencialmente inadequado.

## Arquivos de legenda de vídeo {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

É possível encapsular arquivos de legenda de vídeo (WebVTT), CSS ou qualquer arquivo de texto no formato JSONP. A resposta JSON é descrita abaixo.

* Para arquivos WebVTT, o tipo mime da resposta é text/javascript. JSON não é retornado; em vez disso, é retornado o JavaScript que chama um método com JSON. A ID e o manipulador são opcionais.
* Para arquivos CSS, o tipo mime da resposta é text/javascript. A ID e o manipulador são opcionais.
* Por padrão, a codificação UTF-8 é aplicada para garantir que ela seja decodificada corretamente. O limite de tamanho padrão é de 2 MB.

Também é possível usar rastreamentos para outros tipos de metadados cronometrados. Os dados de origem de cada elemento de rastreamento são um arquivo de texto composto de uma lista de dicas cronometradas. As dicas podem incluir dados em formatos como JSON ou CSV.

Consulte [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) para obter mais informações sobre o formato JSONP.

Consulte [www.json.org](https://www.json.org/json-en.html) para obter mais informações sobre o formato JSON.

## Consulte também {#section-7b28631016044a22a3a6762fd64771e9}

[tipo=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Referência do Catálogo de Imagens](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
